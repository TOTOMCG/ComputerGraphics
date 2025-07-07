Имеется кросс-компилированный pre_compiled_triangle.exe для Windows (должен работать). Но это не очень безопасно и этично поэтому:

Пример для сборки через CMake для MinGW (cmd bash): '\n'
cd build
cmake -G "MinGW Makefiles" .. // По идее можно любой другой компилятор
cmake --build .

В build должен создаться triangles.exe из исходников. 

P.S. Я все равно не на этом треке, но попытаться стоило
