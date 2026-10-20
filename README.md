# Siege of Lothal - Tower Defense

A C++17 tower-defense game built with SFML. Defend the castle against enemy waves by placing towers, following enemy paths, and upgrading your defenses.

## Features

- Tower placement and inventory system
- Enemy waves with path-following movement
- Tower upgrades and upgrade branches
- Tiled orthogonal map rendering
- Mouse-based interaction and real-time rendering
- Project-local textures, fonts, map, and tileset assets
- No bundled music or other audio files

## Screenshots

### Gameplay

![Gameplay screen](screenshots/game-screen.png)

### Main menu

![Main menu screen](screenshots/play-window.png)

## Technology

- C++17
- Visual Studio 2022
- SFML 3
- tmxlite
- TGUI and pugixml project dependencies

## Getting Started

### Prerequisites

- Windows 10 or later
- Visual Studio 2022 with the Desktop development with C++ workload
- SFML 3 and the other dependencies configured for the project

The Visual Studio project currently references dependency folders under `C:\Libraries`. If those dependencies are installed elsewhere, update the include and library paths in the project properties.

### Build and Run

1. Clone the repository:

```bash
git clone https://github.com/Rafi-Sojan/Siege-of-Lothal-Tower-Defense-Game.git
```

2. Open `tower-defense-main/tower-defense-main.sln` in Visual Studio.

3. Select `Release` and `x64`.

4. Build and run the solution.

The project copies the `assets/` folder to the build output automatically. Runtime assets are loaded from paths such as `assets/maps/map-final-2.tmx` and `assets/textures/`.

## Controls

| Action | Input |
| --- | --- |
| Place or interact with towers | Left mouse button |
| Open inventory | `L` |
| Open tower upgrade window | Right mouse button on a tower |
| Choose upgrade branch | `1`, `2`, or `3` |
| Close the current panel | `Escape` or `P` where applicable |
| Zoom in | `I` |
| Zoom out or reset zoom | `O` |
| Open settings screen | `Z` |
| Close settings screen | `M` |

## Project Structure

```text
Tower-Defense-Game/
├── .gitignore
├── .gitattributes
├── README.md
├── screenshots/
│   ├── game-screen.png
│   └── play-window.png
└── tower-defense-main/
    ├── tower-defense-main.sln
    └── tower-defense-main/
        ├── game-main.cpp
        ├── SFMLOrthogonalLayer.hpp
        ├── game.rc
        ├── resource.h
        ├── tower-defense-main.vcxproj
        └── assets/
            ├── fonts/
            ├── maps/
            ├── textures/
            └── tilesets/
```

Generated Visual Studio caches, build outputs, and distribution packages are excluded by `.gitignore`.

## Publishing a Windows Package

Build the `Release | x64` configuration, then distribute the ZIP package containing:

- `tower-defense-main.exe`
- Required SFML runtime DLLs
- The complete `assets/` folder

The generated package is placed under `dist/` locally and is ignored by Git.

## License and Asset Credits

No software license is currently included. Confirm the licenses or permissions for all third-party graphics, fonts, and other assets before redistributing the game.

## Author

Rafi Sojan
