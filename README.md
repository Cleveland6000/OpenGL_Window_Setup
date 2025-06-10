# OpenGL Window Setup

This repository provides a basic setup for creating an OpenGL window using GLFW and GLAD, with GLM for mathematics. This project is configured for **Visual Studio 2022 on Windows (x64)**.

## Project Structure

```
.
├── .gitattributes
├── .gitignore
├── OpenGL_Window_Setup.sln
└── OpenGL_Window_Setup
    ├── main.cpp
    ├── OpenGL_Window_Setup.vcxproj
    ├── OpenGL_Window_Setup.vcxproj.filters
    └── dependencies
        ├── include
        │   ├── glad/
        │   ├── GLFW/
        │   └── glm/
        └── lib
            └── glad.c
```

- `OpenGL_Window_Setup.sln`: Visual Studio solution file.
- `OpenGL_Window_Setup/`: Project directory.
    - `main.cpp`: The main application source file.
    - `OpenGL_Window_Setup.vcxproj`: Visual Studio project file.
    - `OpenGL_Window_Setup.vcxproj.filters`: Visual Studio filter definitions for organizing files in Solution Explorer.
    - `dependencies/`: Contains third-party libraries.
        - `include/`: Header files for GLAD, GLFW, and GLM.
        - `lib/`: Source file for GLAD.

## Getting Started

Follow these steps to set up and run the project:

### 1. Prerequisites

Before you begin, ensure you have the following installed:

- **Visual Studio 2022** (with "Desktop development with C++" workload installed).
- **Git** (optional, but recommended for cloning the repository).

### 2. Clone the Repository (Optional, if you downloaded manually)

If you have Git installed, you can clone this repository:

Bash

```
git clone https://github.com/YOUR_USERNAME/OpenGL_Window_Setup.git
cd OpenGL_Window_Setup
```

_(Note: Replace `YOUR_USERNAME/OpenGL_Window_Setup.git` with the actual repository URL if you've forked or moved it.)_

### 3. Download and Configure GLFW

**GLFW is NOT included in this repository and must be downloaded separately.**

1. Go to the official GLFW website: [https://www.glfw.org/download.html](https://www.glfw.org/download.html)
    
2. Download the **pre-compiled binaries for Windows (64-bit)** (e.g., `glfw-3.x.x.bin.WIN64.zip`).
    
3. Extract the downloaded ZIP file.
    
4. Navigate to the extracted GLFW folder. You will find:
    
    - `include/GLFW/`: This contains `glfw3.h` and `glfw3native.h`.
    - `lib/MSVC/`: This contains the compiled `.lib` files (e.g., `glfw3.lib`).
5. **Copy the GLFW files into your project:**
    
    - Copy the `glfw3.h` and `glfw3native.h` files from `GLFW/include/GLFW/` into your project's `OpenGL_Window_Setup/dependencies/include/GLFW/` folder.
    - Copy the `glfw3.lib` file (found in `GLFW/lib/MSVC/`) into a new folder: `OpenGL_Window_Setup/dependencies/lib/`. Create the `lib` folder if it doesn't exist.
        - _(You should now have `OpenGL_Window_Setup/dependencies/lib/glad.c` and `OpenGL_Window_Setup/dependencies/lib/glfw3.lib`)_

### 4. GLM (Included)

The GLM (OpenGL Mathematics) header files are already included in `OpenGL_Window_Setup/dependencies/include/glm/`. No additional steps are required for GLM.

### 5. Open and Build the Project in Visual Studio 2022

1. Open `OpenGL_Window_Setup.sln` in Visual Studio 2022.
2. Ensure the solution platform is set to **x64** (usually located in the toolbar or `Build > Configuration Manager`).
3. Build the solution (`Build > Build Solution` or `Ctrl+Shift+B`).

If everything is set up correctly, the project should build without errors.

## Running the Application

After a successful build, you can run the application by pressing `F5` or `Debug > Start Debugging`. A simple OpenGL window should appear.
