# Mersenne Twister Parallel
It is the paralell version of my previous repository. See the previous repository [here](https://github.com/errmsg/MersenneTwisterSerialCpp.git).
Based on the code written by Takuji Nishimura and Makoto Matsumoto. Code is initially writing in C and ported to C++ (by me). Algorithm is 64 bit. See "mt_serial_h" for more.

## Installation
```bash
$ cd to/path/that/you/wish
$ git clone
```

## Dependencies
* C++ STL
* Catch (included)

## Compilation
CMake is used to generate make files. It is strongly advised to run CMake in *build* directory.
When CMake is done generating make files, you can use make to compile the sources files. After that
you can run the executables (as shown below).
**IMPORTANT NOTE:** For now make files only compile catchTestSerial.cpp.

```bash
   $ cd build
   $ cmake -G "Unix Makefiles" ..
   $ make
   $ ./catchTestSerial
```
For now just stick with the manual way, in OS X

```bash
   $ cd tests
   $ clang++ paralell.cpp -o parallel -framework OpenCL
   $ ./parallel
```
in Linux, (asuming you have properly installed OpenCL)

```bash
   $ cd tests
   $ g++ paralell.cpp -o parallel -lOpenCL
   $ ./parallel
```

## Testing
Cacth is used for testing (not implemented for parallel yet). See *tests*. Test files are compiled with CMake.

## Tasks
- [ ] Testing for Mersenne twister (both paralell and serial) via [catch](https://github.com/philsquared/Catch) framework.
- [ ] Include chrono library and calcuate how much time is needed for both serial and parallel execution.
- [ ] Comparing the serial and parallel version with time stamps.

## Notes
The serially computed version of the algorithm is [here](https://github.com/errmsg/MersenneTwisterSerialCpp.git).

## License
MIT (see LICENSE)
