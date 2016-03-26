# GoPythonDLLWrapper
A Go program that wraps python dll and scripts to ease up the python program distribution for windows.

### Target machine and package
  - 32bit Windows, Python 3.4 (To be in compatable with Windows XP)

> This can be easily modified by replacing files and directories like `python.exe`, `pythonXY.dll`, `msvcrXXX.dll`, `lib` under `bin` directory with any version of Python you want. They're usually in Python installation directory or `%WINDIR%\System32\`.

### Possible application
  - Instantly runnable Go & Python program packages without asking user to setup Python before.
  - Multiple Python interpreters running seperately by Go routines

### Usage
  1. Build with `go build`.
  2. Put built `GoPythonDLLWrapper.exe` in `bin` directory to let it get along with other dependent files.
  2. Just think built `GoPythonDLLWrapper.exe` as the same as `python.exe`. Which means you can just `./GoPythonDLLWrapper` to open python REPL or `./GoPythonDLLWrapper main.py hello` to run `main.py` script with argument `hello` in PowerShell. (or just `GoPythonDLLWrapper` and `GoPythonDLLWrapper main.py hello` in CMD)
  3. Feel free to modify `main.go` on your need. ([Related docs](https://docs.python.org/3/c-api/index.html)) You can also rename `GoPythonDLLWrapper.exe` to anything you want.

### Note
> While everyone thinks it's able to, doing so is entirely burdened on the person who is awaken to.
