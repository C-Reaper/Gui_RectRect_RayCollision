# Project README

## Overview
This project demonstrates a simple graphical user interface (GUI) application that allows users to test ray collision detection between rectangles using C and a custom-made GUI library.

## Features
- Ray collision detection between two rectangles.
- Basic GUI for visualization and input.
- Cross-platform support via Makefiles.

## Project Structure
```
Gui_RectRect_RayCollision/
├── build/              # .exe files produced by Main.c
├── src/                # source code directory
│   ├── Main.c          # entry point of the application
│   └── Gui.h           # header file for GUI library functions
├── Makefile.linux      # Linux build configuration
├── Makefile.windows    # Windows build configuration
├── Makefile.wine       # Wine build configuration
└── README.md           # this file
```

### Prerequisites
- C/C++ Compiler and Debugger (GCC)
- Make utility
- Standard development tools
- X11 libraries for Linux

## Build & Run
### Building on Linux
To build the application on Linux, navigate to the project directory and run:
```bash
make -f Makefile.linux all
```
For a clean rebuild:
```bash
make -f Makefile.linux clean
make -f Makefile.linux all
```

### Running on Linux
After building, you can execute the application using:
```bash
./build/Main
```

### Building and Running on Windows
To build the application on Windows, navigate to the project directory and run:
```bash
make -f Makefile.windows all
```
For a clean rebuild:
```bash
make -f Makefile.windows clean
make -f Makefile.windows all
```

After building, you can execute the application using:
```bash
./build/Main.exe
```

### Building on Wine
To build and run the application using Wine on Linux, navigate to the project directory and run:
```bash
make -f Makefile.wine all
```
For a clean rebuild:
```bash
make -f Makefile.wine clean
make -f Makefile.wine all
```

After building, you can execute the application using:
```bash
wine build/Main.exe
```

### Building for WebAssembly
To build the application for WebAssembly using Emscripten, navigate to the project directory and run:
```bash
make -f Makefile.web all
```
For a clean rebuild:
```bash
make -f Makefile.web clean
make -f Makefile.web all
```

After building, you can serve the application on a web server or use Emscripten's emrun to host it locally:
```bash
emrun --no_browser --port 8080 build/index.html
```

This README provides a straightforward overview of how to build and run the project across different platforms.