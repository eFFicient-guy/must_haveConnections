# GCC 15 

`GCC 15` is a release of the GNU compiler collection.It improves compiler diagnostics, optimization, hardware support, and support for newer versions of c and c++

For C, GCC 15 uses GNU c23 as its default language standard.

For c++, g++ 15 still uses GNU c++17 by default.Newer standards must be selected explicitly, for example : `-std=c++23` enables c++23

GCC 15 includes incremental link-time optimization through 
`-flto-incremental=`, which can reduce recompilation time when making small changes to programs that use LTO

