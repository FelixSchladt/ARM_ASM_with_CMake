# ARM GCC installieren
Webseite:
https://gnutoolchains.com/arm-eabi/

Nach z.B. C:\Toolchains\

**WICHTIG:** zu PATH hinzufügen (lassen)

# CMake vorbereiten
In den Unterordner _Build_ vorbereiten:
````
cmake -G"MinGW Makefiles" -DCMAKE_BUILD_TYPE=Debug -DCMAKE_TOOLCHAIN_FILE:PATH="toolchain.cmake" -S . -B Build
````

# Kompilieren
In den Build-Ordner wechseln:
````
X:\Test Assembler>cd Build
````
Bauen
````
X:\Test Assembler\Build>cmake --build .
````