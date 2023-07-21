# Shellcode Loader

This is a simple C++ project that demonstrates how to load and execute shellcode into a target process using remote thread injection. The project consists of a loader that injects a sample `calc.exe` shellcode into a target process, in this case, `notepad.exe`. The `calc.exe` shellcode will launch the Windows Calculator when executed in the context of the target process.

## Table of Contents
- [Introduction](#introduction)
- [Requirements](#requirements)
- [Usage](#usage)
- [License](#license)

## Introduction

This project showcases the usage of the Windows API functions `CreateToolhelp32Snapshot`, `Process32First`, `Process32Next`, `OpenProcess`, `VirtualAllocEx`, `WriteProcessMemory`, and `CreateRemoteThread` to perform remote thread injection. It demonstrates how to find the Process ID of the target process (`notepad.exe` in this case) and load the sample shellcode into its memory space.

The main files in this project are:
- `main.cpp`: Contains the main logic for enumerating processes, finding the target process, and loading the shellcode.

## Requirements

To run the project, you need the following:

- A Windows-based operating system (tested on Windows 10).
- A C++ compiler that supports C++11 standard or later (e.g., Visual Studio, MinGW, etc.).

## Usage

1. Clone or download this repository to your local machine.

2. Open the project in your preferred C++ development environment.

3. Build the project to generate the executable.

4. Start notepad.exe.
   
5. Run the executable.

Upon running the program, it will find the Process ID of the target process ("notepad.exe") using `EnumerateProcess` function. It will then load and execute the shellcode in the memory space of the target process using `LoadShellcode` function.

**Note**: Make sure to use this code responsibly and only on systems you have proper authorization to access.

## License

This project is licensed under the [MIT License](LICENSE). Feel free to use, modify, and distribute this code for your own purposes.

