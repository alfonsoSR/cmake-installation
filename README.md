# CMAKE INSTALLATION EXAMPLE

```bash
cd tudat
make b
make c
make i
cd ..
cd test
make c
./main
```
libtudat.a will be added to ${CMAKE_INSTALL_PREFIX}/lib
types.hpp will be added to ${CMAKE_INSTALL_PREFIX}/include/tudat
