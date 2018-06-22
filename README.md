# Drawing the national flag of Bangladesh
## Using OpenGL and C++

### Required Libraries
- OpenGL 4.2 (minimum)
- GLUT

### Building

- On macOS, open in XCode as project, add OpenGL and GLUT libraries from project properties. Build and Run.

- You can also use `-framework GLUT -framework OpenGL` flag while compiling from command line (macOS only).

- On linux : use the flags provided by the opengl and glut libs built for your distro.

- On Windows, install GLUT and add headers and linkers to your project in Visual Studio or Preferable IDE. 

- If you're using CLion and/or building CMAKE, then use the following config for your cmake.txt file

```cpp
cmake_minimum_required(VERSION 3.6)
project(project_name)

set(CMAKE_CXX_STANDARD 11)

if(APPLE)
    find_package(OpenGL REQUIRED)
    include_directories(${OpenGL_INCLUDE_DIRS})
    find_package(GLUT REQUIRED)
    include_directories(${GLUT_INCLUDE_DIRS})

    set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -framework GLUT -framework OpenGL")
else()
    set(CMAKE_CXX_LINK_EXECUTABLE "${CMAKE_CXX_LINK_EXECUTABLE} -lGL -lGLU -lglut")
endif()

add_executable(project_name ${SOURCE_FILES})
```

