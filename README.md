# nelua-raylib
[Raylib](https://github.com/raysan5/raylib/) bindings for the [Nelua](https://github.com/edubart/nelua-lang) programming language.

## Table Of Contents
- [nelua-glfw](https://github.com/AKDev21/nelua-raylib)
    - [Special Thanks](https://github.com/AKDev21/nelua-raylib#special-thanks)
    - [Pre requisite](https://github.com/AKDev21/nelua-raylib#pre-requisite)
    - [Getting Started](https://github.com/AKDev21/nelua-raylib#getting-started)
    - [Example](https://github.com/AKDev21/nelua-raylib#example)
    - [Contact](https://github.com/AKDev21/nelua-raylib#contact)

### Special Thanks
- [Eduardo Bart](https://github.com/edubart/)
    - for creating nelua-decl which is used for generating 95% of the bindings.   
    - for creating the nelua programming langauge.

### Pre requisite
- You should have ``raylib.h`` and ``libraylib`` in the current working directory or in your environment's PATH variable, which you download from the [raylib repository](https://github.com/raysan5/raylib/releases/tag/3.7.0).

### Getting Started
- Copy paste the ``raylib.nelua`` file in the current working directory.
- Create a ``main.nelua`` file and copy the code given in the [example section](https://github.com/AKDev21/nelua-glfw#example).
- Open a command prompt or terminal and run the following command.
```
nelua main.nelua --cflags=" -I . -L . "
```

### Example
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

### Contact
- [Nelua Discord Server](https://discord.com/invite/7aaGeG7)