# Drawing the national flag on Bangladesh
## Using OpenGL and C++

### Required Libraries
- OpenGL 4.2 (minimum)
- GLUT

### Usage

- On macOS, open in XCode as project, add OpenGL and GLUT libraries from project properties. Build and Run.

- You can also use `-lgl` and `-lglut` flags while compiling from command line.

- On linux : use the flags provided by the opengl and glut libs built for your distro.

- On Windows, install GLUT and add headers and linkers to your project in Visual Studio or Preferable IDE. 

- If you're using CLion and/or building CMAKE, make sure you add compiler flags : 
```bash
-lgl -lglut
```