# validator-keys-tool

xahaud validator key generation tool


## Build
The build requirements and commands are the exact same as
[those for rippled](https://github.com/XRPLF/rippled/blob/develop/BUILD.md).

If you do not have package `xrpl` in your local Conan cache, it can be added by following the instructions in the [BUILD.md](https://github.com/XRPLF/rippled/blob/master/BUILD.md#patched-recipes) file in the rippled GitHub repository.

Example build instructions:

```
git clone [this repo]
cd [this repo]
mkdir .build
cd .build
conan install .. --output-folder . --build missing
cmake -DCMAKE_POLICY_DEFAULT_CMP0091=NEW \
    -DCMAKE_TOOLCHAIN_FILE:FILEPATH=conan_toolchain.cmake \
    -DCMAKE_BUILD_TYPE=Release \
    ..
cmake --build .
./validator-keys --unittest # or ctest --test-dir .
```


## Guide

[Validator Keys Tool Guide](doc/validator-keys-tool-guide.md)
