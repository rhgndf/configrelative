# wasm-pack with dependencies which bundle C files

## Unsuccessful compilation
There are error messages about not being able to find include files
```
CMAKE=$(pwd)/cmake.sh CFLAGS="-Iinclude -Os -nostdlib -Wl,--no-entry" wasm-pack build
```

## Successful compilation
```
CMAKE=$(pwd)/cmake.sh CFLAGS="-I$(pwd)/include -Os -nostdlib -Wl,--no-entry" wasm-pack build
```
