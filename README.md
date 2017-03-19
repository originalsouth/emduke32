# emduke32
An effort to port duke3d to your web browser by combining eduke32 with emscripten
```
/* By BC van Zuiden -- Leiden, March 2017 */
/* Probably very buggy USE AT OWN RISK this will brick everything you own */
/* NOBODY but YOU is liable for anything that happened in result of using this */
/* WARNING: DON'T RUN THIS PROGRAM THIS WILL DESTROY YOUR COMPUTER AND/OR HOUSE; POSSIBLY BY ALIENS */
/* Any copyrighted piece of code within this code is NOT mine */
/* Inclusion of that code is forced upon me by a scary anonymous guy with a gun*/
/* https://github.com/originalsouth/emduke32 */
```

### About
emduke32 aims to bring duke3d to your web browser by combining eduke32 with emscripten.
It does so by adding emscripten support to the eduke32 makefile system with minimal soure code modifications.

Feel free to reuse and contribute, pull requests are very welcome!
This code is (and forever will be) a work in progress.

### Building
To build the normal eduke32 binary with gcc run:
```
make
```
To build the normal eduke32 binary with clang run:
```
make CLANG=1
```
To build eduke32.js with emcc run:
```
make EMSCRIPTEN=1
```
To build eduke32.html with emcc run:
```
make EMSCRIPTEN=1 HTML=1
```
You can load the html file with a webserver, for instance darkhttpd.
You will have to supply a copy of the original game files `duke3d-folder` yourself they can be pre-loaded as such:
```
make EMSCRIPTEN=1 HTML=1 EMSPRELOAD=<duke3d-folder>
```
The OBJECT files will be removed by running `make clean`

### Acknowledgements
* [duke3d](https://3drealms.com/catalog/duke-nukem-3d_27/)
* [eduke32](http://eduke32.com/) 
* [emscripten](https://github.com/kripken/emscripten)
* [darkhttpd](https://unix4lyfe.org/darkhttpd/)
