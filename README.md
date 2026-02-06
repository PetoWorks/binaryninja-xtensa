# Binary Ninja Xtensa Architecture Plugin

Xtensa machine code decoder & Binary Ninja architecture plugin.

**Build (Linux)**
```
$ git clone https://github.com/PetoWorks/binaryninja-xtensa
$ git clone https://github.com/Vector35/binaryninja-api
$ cd binaryninja-api && cat <PATH_TO>/binaryninja/api_REVISION.txt
$ git checkout <REVISION>
$ git submodule update --init --recursive
$ cd ../binaryninja-xtensa
$ mkdir build
$ cmake -S . -B build -D BN_API_PATH="$(realpath ../binaryninja-api)" -D BN_INSTALL_DIR="<PATH_TO>/binaryninja"
$ cmake --build build
$ ln -sf "$(realpath build/lib/xtensa_arch/libarch_xtensa.so)" "$HOME/.binaryninja/plugins/libarch_xtensa.so"
```


**Build (macOS)**
```
$ git clone https://github.com/PetoWorks/binaryninja-xtensa
$ git clone https://github.com/Vector35/binaryninja-api
$ cd binaryninja-xtensa
$ mkdir build
$ cmake -S build -B build -D BN_API_PATH="$(realpath ../binaryninja-api)"
$ cmake --build build
$ ls build/lib/xtensa_arch/libarch_xtensa.dylib
```

**Build (Windows)**
```
$ git clone https://github.com/PetoWorks/binaryninja-xtensa
$ git clone https://github.com/Vector35/binaryninja-api
$ cd binaryninja-xtensa
$ mkdir build
$ cmake -A x64 -S . -B build -D BN_API_PATH="..\binaryninja-api"
$ cmake --build build --config Release
$ ls build/lib/xtensa_arch/Release/arch_xtensa.dll
```

Big thanks to @emesare to help write this plugin
