# nelua-raylib
[Raylib](https://github.com/raysan5/raylib/) bindings for the [Nelua](https://github.com/edubart/nelua-lang) programming language.

## Gettings Started
You can follow this article for setting up nelua-raylib.

## Special Thanks
- [Eduardo Bart](https://github.com/edubart/)
    - for creating nelua-delc which is used for generating the bindings.   
    - for creating the nelua programming langauge.

## Example
```lua
require "raylib"

-- Initialization
--------------------------------------------------------------------------------------
local screenWidth <comptime> = 800
local screenHeight <comptime> = 450

InitWindow(screenWidth,screenHeight, "raylib-nelua [core] example - basic window")

SetTargetFPS(60)        -- Set our game to run at 60 frames-per-second

--------------------------------------------------------------------------------------

-- Main game loop

while not WindowShouldClose() do        -- Detect window close button or ESC key

    -- Update
    ----------------------------------------------------------------------------------
    -- TODO: Update your variables here
    ----------------------------------------------------------------------------------

    -- Draw
    ----------------------------------------------------------------------------------

    BeginDrawing()

        ClearBackground(RAYWHITE)

        DrawText("Congrats! You created your first window!", 190, 200, 20, LIGHTGRAY)

    EndDrawing()
    -----------------------------------------------------------------------------------
end

-- De-Initialization
-------------------------------------------------------------------------------------
CloseWindow()       -- Close window and OpenGL context
-------------------------------------------------------------------------------------

```