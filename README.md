# validator-keys-tool

xahaud validator key generation tool


## Build
The build requirements and commands are the same as [those for xahaud](https://github.com/Xahau/xahaud/blob/dev/BUILD.md).


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
