
## What are OpenGL loading libraries? 

What's interesting, OpenGL is already preinstalled in your Windows, but it's still necesary to configure a loading library. Loading library is responsible for loading pointers to OpenGL functions at runtime. This way, you don't need to load OpenGL functions manually.

## GLAD configuration 

a) Go to [official Glad website](https://glad.dav1d.de/) and generate GLAD for the newest version of OpenGL (OpenGL 4.6 was released in 2017, so I assume that you don't need to download earlier version). Click on glad.zip in order to start download and then unzip the package. 
![1a](https://github.com/knitterJ/the-easiest-way-to-start-using-OpenGL-MinGW-glfw-or-freeglut-glad-or-glew-no-cmake/blob/main/Windows/3.GLAD-or-GLEW-alternatively/a.png)

b) Enter the newly created folder and copy 2 folders located in the `include` folder (meaning KHR and glad) to `C:\MinGW\include`

c) Open new command prompt and navigate to `src` folder. Then introduce the following command: 




















