# Exercise Prerequisites
### rp_01_compilers_and_build_systems

## Installing GCC on Ubuntu (Compiler)

The default Ubuntu repositories contain a meta-package named  `build-essential`  that contains the GCC compiler and a lot of libraries and other utilities required for compiling software.

Perform the steps below to install the GCC Compiler Ubuntu 18.04/20.04:

1.  Start by updating the packages list:
    
    ```
    sudo apt update
    ```
    
2.  Install the  `build-essential`  package by typing:
    
    ```
    sudo apt install build-essential
    ```
    
    The command installs a bunch of new packages including  `gcc`,  `g++`  and  `make`.
    
    You may also want to install the manual pages about using GNU/Linux for development:
    
    ```
    sudo apt-get install manpages-dev
    ```
    
3.  To validate that the GCC compiler is successfully installed, use the  `gcc --version`  command which prints the GCC version:
    
    ```
    gcc --version
    ```
    
    The default version of GCC available in the Ubuntu 18.04 repositories is  `7.4.0`:
    
    ```output
    gcc (Ubuntu 7.4.0-1ubuntu1~18.04) 7.4.0
    Copyright (C) 2017 Free Software Foundation, Inc.
    This is free software; see the source for copying conditions.  There is NO
    warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
    ```
	  The default version of GCC available in the Ubuntu 20.04 repositories is  `9.3.0`:
	```output 
	gcc (Ubuntu 9.3.0-17ubuntu1~20.04) 9.3.0
	Copyright (C) 2019 Free Software Foundation, Inc.
	This is free software; see the source for copying conditions.  There is NO
	warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
	```

## Installing Eigen

Eigen is a C++ template library for linear algebra: matrices, vectors, numerical solvers, and related algorithms. We will explain better this when we will use the library. At the moment is enough to install it. On Ubuntu 18.04/20.04 execute the following command on the terminal:
```
sudo apt install libeigen3-dev
```
Check that package has been installed correctly using `pkg-config`:
```
pkg-config --list-all | grep eigen
```

## Hint - Debugging with CMakeLists
Often, especially for very large projects and builds you have errors :)  hence it is very helpful having a way of debugging. With CMakeLists you can print a message by typing (in the `CMakeLists.txt`):  
```
message("my variable value:"  ${SOME_VARS})
```
or you can actually write if-statement to redirect the user to human readable errors
```
if(NOT SOME_VARS)
message(FATAL_ERROR "This variable is not set!")
endif()
```

Here the FLAG `FATAL_ERROR` will exit the compilation! Please refer to the [docs](https://cmake.org/cmake/help/latest/command/message.html) for more info and flags! 

 
### Now you are ready to write your (first maybe) nested CMakeLists :)