# This is a minimal CMakeLists files which include the Yoctopuce C++ lib.
cmake_minimum_required (VERSION 3.16)
project (Demo)

# Add the Sources subfolder of the Yoctopuce C++ library.
add_subdirectory (../yoctolib_cpp/Sources compiled_yoctolib)

# Add executable called "demo" that is built from the source files "main.pp".
add_executable (demo main.cpp)

# Link the executable to the Yoctopuce C++ library (YoctoLib).
target_link_libraries (demo LINK_PUBLIC YoctoLib)
