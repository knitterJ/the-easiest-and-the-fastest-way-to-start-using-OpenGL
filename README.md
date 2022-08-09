## Intro

Have you ever wanted to run simple Hello-Triangle program, that contains OpenGL functions and you had to go through the configuration hell? 
If so, this tutorial is prepared for you. I explain how to configure OpenGL for both Windows and Linux without the necesity to install Visual Studio or configure Cmake.

## How you should think of OpenGL?  
In a simplified way, think of OpenGL as a set of functions that are operating system agnostic.

In order to use OpenGL functions, it's necesary to configure two extra libraries, which are tweaked for your operating system:
1) [**Window Toolkit**](https://www.opengl.org/resources/libraries/windowtoolkits/) like GLFW or Freeglut<br>
2) [**Function Loader**](https://stackoverflow.com/questions/27873784/when-do-i-need-to-use-an-opengl-function-loader) like GLAD or GLEW<br>
  
