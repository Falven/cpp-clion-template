cpp_clion_template
====================

###### Falven
_________

Template project for Clion C++ projects.

This project uses CMake for cross-platform compliance.

## Building - Out of Source (Recommended)

I recommend you build this project out-of-source so source files don't get mixed with build files and cause problems.
What this means is placing the build files outside of the project's source root directory. 

1. Create a directory outside of this project where binaries will be built.
    * If building with a CMake GUI application:
        1. Right click anywhere outside the project and make a new folder `cpp_clion_template_build/`.
    * If building through the cmake CLI (command line interface):
        1. `mkdir cpp_clion_template_build/`
2. Set appropriate directories; depending on your CMake utility:
    * If building with a CMake GUI application:
        1. Set the 'source' directory to the top-level directory of this project.
        2. Set the 'build' directory to the directory you created in step 1.
    * If building through a CMake CLI (command line interface):
        1. cd to the directory we created in step 1. `cpp_clion_template_build/` (important!)
3. Set appropriate cmake variables
    * If building with a CMake GUI application:
        1. Set appropriate variable values in 'cache values'.
    * If building through a CMake CLI (command line interface):
        1. You can pass options to CMake CLI using the `-D <var>:<type>=<value>` command.
        2. `cmake [options] <path-to-source>`
4. Create build tools for the project.
    * If building with a CMake GUI application:
        1.  Select configure and select an appropriate generator, where the generator is the type of build project you would like to create, and completely dependent on your platform.
    * If building through the cmake CLI (command line interface):
        1. `cmake -G <generator-name>` where generator is the type of project you would like to create, and completely dependent on your platform. Make sure you are in the `cpp_clion_template_build/` directory when you do this.
            1. To see available options simply type `cmake -G`
5. Build the project using the generated build tools
    * For example, if you generated a `Makefile` type `make`.

### Example
Generating a Unix Makefile
1. `mkdir cpp_clion_template_build/ && cd cpp_clion_template_build/`
2. `cmake -G "Unix Makefiles" -DCMAKE_BUILD_TYPE=Debug ../cpp_clion_template/`


