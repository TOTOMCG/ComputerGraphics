Установить mingw для windows: https://www.mingw-w64.org/downloads/

Добавить mingw в PATH для корректной работы.

Пример для сборки через CMake для MinGW:

mkdir build && cd build
cmake -G "MinGW Makefiles" ..
cmake --build .
В build должны появится: plain_texture.exe (просто текстура), texture45.exe (текстура, повёрнутая на 45 градусов), 2texture.exe (две текстуры), rotate.exe (крутится!!!).
