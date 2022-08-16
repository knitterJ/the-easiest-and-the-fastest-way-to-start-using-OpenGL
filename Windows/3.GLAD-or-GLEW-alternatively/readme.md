
## What are OpenGL loading libraries? 

What's interesting, OpenGL is preinstalled in your Windows, but it's still necesary to configure a loading library. Loading library is responsible for loading pointers to OpenGL functions at a runtime. This way, you don't need to load OpenGL functions manually. If you want to/need to configure GLEW instead of Glad go [here]().

## GLAD configuration 

1/6) Go to [official Glad website](https://glad.dav1d.de/) and generate GLAD for the newest version of OpenGL (OpenGL 4.6 was released in 2017, so I assume that you don't need to download earlier version). Click on glad.zip in order to start download and then unzip the package. 
![1a](https://github.com/knitterJ/the-easiest-way-to-start-using-OpenGL-MinGW-glfw-or-freeglut-glad-or-glew-no-cmake/blob/main/Windows/3.GLAD-or-GLEW-alternatively/a.png)

2/6) Enter the newly created folder and copy 2 folders located in the `include` folder (meaning KHR and glad) to `C:\MinGW\include`

// Gif placeholder

3/6) Open new command prompt and navigate to `src` folder where glad.c file is located. Then introduce the following command: 
`gcc -c glad.c`

and right after the next command: 

`ar rcs libglad.a glad.o`

// Gif placeholder 

This way static library, which can be used universally in every project, was created. 

4/6) Move libglad.a file to `C:\MinGW\lib`

// Screenshot placeholder 

5/6) Now it's possible to compile C++ programs with the reference to `-lglad` library 

6/6) Test the configuration with the following file (downloadable easily from [here]()): 

// Code placeholder

 `g++ main.cpp -lglad -lglfw3`

image placeholder 

This way you configured successfully libraries, which allows you to use OpenGL. 
