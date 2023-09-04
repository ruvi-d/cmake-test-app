```
rm -rf build/ && mkdir build && cd build
export HELLOLIB_ROOT_PATH=/home/ruvi/projects/test/test-lib/build/install
cmake -DCMAKE_INSTALL_PREFIX="$(pwd)/install" ..
cmake --build .
cmake --install .
```