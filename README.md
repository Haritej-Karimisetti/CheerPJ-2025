# Retro GameBoy Web Console (CheerpJ Powered)

This project is a fully interactive GameBoy-style web console built
using only HTML, CSS, and vanilla JavaScript. It is capable of running
Java `.jar` games directly inside the browser using CheerpJ 3.0, without
requiring any local Java installation.

The UI simulates the classic handheld console, including a power button,
LED indicator, startup animation, cartridge loading, and fully
functional A/B, D-Pad, Start, and Select buttons. The project also
includes a built-in game loader for `.jar` files.

## Features

### Console Simulation

-   Retro-styled console casing and layout
-   Scanline LCD effect
-   Power on/off system
-   Boot animation with "Nintendo"-style scroll
-   Cartridge insertion menu

### CheerpJ Java Runtime Integration

-   Runs `.jar` games inside the browser
-   Auto-scaled canvas display
-   Single initialization for efficient performance

### Virtual Controls

-   D-Pad (Up/Down/Left/Right)
-   A and B buttons
-   Start and Select buttons
-   Press animations
-   Keyboard event emulation
-   Mobile touch support

### Cartridge System

-   Interactive cartridge slot
-   Loads `.jar` games from the `/games/` folder
-   Loading feedback ("READING CARTRIDGE...")
-   Reset console button with auto power-cycle

## Project Structure

    index.html
    games/
       snake.jar
       space.jar

## How the Project Works

### 1. CheerpJ Integration

CheerpJ is loaded using:

    <script src="https://cjrtnc.leaningtech.com/3.0/cj3loader.js"></script>

### 2. Power System

The power switch toggles LED state, screen color, boot animation, and
menu visibility.

### 3. Cartridge Loading

    cheerpjCreateDisplay(640, 480, element);
    cheerpjRunJar("/app/games/mygame.jar");

### 4. Controls

HTML buttons emit keyboard events (`Arrow` keys, `Z`, `X`, `Enter`,
`Shift`).

## Installation and Setup

### Run Locally

Open `index.html` directly in any browser.

### Deploy Online

Works on GitHub Pages, Vercel, Netlify, Render, Replit, or any static
host.\
Required structure:

    /index.html
    /games/*.jar

## Adding Your Own Games

Place your `.jar` file into `games/` and add a button:

    <button class="game-btn" onclick="loadGame('games/myGame.jar', this)">
      Cartridge: My Game
    </button>

## Compatibility

  Component                 Supported
  ------------------------- -----------------------
  Desktop Browsers          Chrome, Edge, Firefox
  Mobile Browsers           No
  Requires Java Installed   No
  Works Offline             No

## Known Issues

-   Some `.jar` files may not work if they use unsupported AWT/Swing
    features.
-   Restarting a game may require "Reset Console".
-   Refreshing the page resets CheerpJ.

## Contributors

-   Krithik Sharan Suresh Alagianayagi
-   Asjad Moiz Khan
-   Uday Reddy Kiran Mule
-   Haritej Karmisetti

## License

MIT License. CheerpJ licensing belongs to Leaning Technologies.

## Credits

-   CheerpJ by Leaning Technologies
-   GameBoy aesthetic inspiration
-   Java game developers
