Установить mingw для windows: https://www.mingw-w64.org/downloads/

Добавить mingw в PATH для корректной работы.

Пример для сборки через CMake для MinGW:
```bash
mkdir build && cd build
cmake -G "MinGW Makefiles" ..
cmake --build .
```
В build должен появиться cube.exe
