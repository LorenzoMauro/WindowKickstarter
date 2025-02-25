
**This is a GitHub template repository.** Click "Use this template" to create a new project based on this setup.

# WindowKickstarter

A minimal CMake-based starter project for cross-platform window creation using GLFW, GLAD, and OpenGL.  

- [Features](#features)
- [Getting Started](#getting-started)
  - [Clone the Repository](#clone-the-repository)
  - [Install Dependencies](#install-dependencies)
  - [Build Instructions](#build-instructions)
    - [Nvim with cmake-tools.nvim](#nvim-with-cmake-toolsnvim)
    - [Command Line](#command-line)
    - [Visual Studio](#visual-studio-integration)

## Features
- **Cross-platform**: Works on Windows, Linux, and macOS.
- **CMake-based**: Easily configurable and extendable.
- **Vcpkg integration**: Dependencies managed via vcpkg.
- **GLFW & GLAD**: Provides a basic OpenGL window setup.
- **CMake Presets**: Pre-configured build settings for Debug and Release.
- **Visual Studio Integration**: Open the project folder directly in Visual Studio for automatic CMake configuration.

## Getting Started

### Clone the Repository
```bash
git clone --recursive https://github.com/LorenzoMauro/WindowKickstarter.git
cd WindowKickstarter
```
> **Note**: The `--recursive` flag is needed to fetch the vcpkg submodule. If you forgot, run:
> ```bash
> git submodule update --init --recursive
> ```

### Install Dependencies
Ensure you have:
- **CMake (3.15+)**
- **Ninja** (recommended but optional)
- **A C++ compiler** (MSVC, Clang, or GCC)
- **Vcpkg** (handled as a submodule)

### Build Instructions

### Nvim with cmake-tools.nvim
The project is configured to work with [nvim](https://neovim.io/) and [cmake-tools.nvim](https://github.com/Civitasv/cmake-tools.nvim), just open the project folder in nvim and run `:CMakeConfigure`, `:CMakeBuild` and `:CMakeRun`.

### Command Line

**For Debug Build**:
```bash
cmake --preset debug
cmake --build --preset debug
```

**For Release Build**:
```bash
cmake --preset release
cmake --build --preset release
```

Run the compiled executable:
```bash
./out/Debug/src/Window # Debug mode (+ .exe on Windows)
./out/Release/src/Window # Release mode (+ .exe on Windows)
```
### Visual Studio
1. Open **Visual Studio** (2019 or newer).
2. Select **"Open a Local Folder"** and choose the WindowKickstarter directory.
3. Visual Studio will detect `CMakeLists.txt` and configure automatically.
4. Build and run directly from the IDE.
