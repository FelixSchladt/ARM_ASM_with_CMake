# Windows

## ARM GCC installieren

Webseite:
https://gnutoolchains.com/arm-eabi/

Nach z.B. C:\Toolchains\

**WICHTIG:** zu PATH hinzufügen (lassen)

## CMake vorbereiten
In den Unterordner _Build_ vorbereiten:
````shell
cmake -G"MinGW Makefiles" -DCMAKE_BUILD_TYPE=Debug -DCMAKE_TOOLCHAIN_FILE:PATH="toolchain.cmake" -S . -B Build
````

## Kompilieren
In den Build-Ordner wechseln:
````shell
X:\Test Assembler>cd Build
````
Bauen
````shell
X:\Test Assembler\Build>cmake --build .
````

# Unix

## ARM GCC installieren

Ubuntu
```shell
sudo apt install gcc-arm-none-eabi cmake
```

Arch
```shell
yay -S gcc-arm-none-eabi-bin 
sudo pacman -S cmake
```

macOS
```shell
brew install gcc-arm-embedded
```

## CMake vorbereiten

```shell
cmake -DCMAKE_BUILD_TYPE=Debug -DCMAKE_TOOLCHAIN_FILE:PATH="toolchain.cmake" -S . -B Build
```

## Kompilieren

In den Build-Ordner wechseln:
```shell
cd Build
```

Bauen:
```shell
cmake --build .
```
