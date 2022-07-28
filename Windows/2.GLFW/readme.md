Next item to configure is GLFW. Based on the official specification:

GLFW is a toolkit built on top of OpenGL that handles tasks, such as opening an OpenGL window and reading keyboard and mouse input.
So basically, if you want to display a window and see any result, toolkit like GLFW needs to be properly configured. List of alternative toolkits can be found here: https://www.opengl.org/resources/libraries/windowtoolkits/ 

a) Download 32-bit Windows binaries from official glfw website https://www.glfw.org/download.html and unpack it,

b) Go to include folder, copy GLFW and paste it to C:\MinGW\include

c) Next go to lib-mingw folder:
copy glfw3.dll and paste it to C:\MinGW\bin

d) From the same lib-mingw folder:
copy libglfw3dll.a and paste it to C:\MinGW\lib

WARNING! DON'T COMPILE YOUR CODE WITH -lglfw3 like many tutorials indicate, because libglfw3.a is a static library that is not correctly configured for gcc. More to read about it in this Stackoverflow thread: https://stackoverflow.com/questions/22623087/undefined-reference-errors-when-linking-glfw-on-mingw

If it yields errors check the configuration in the following steps



If you want to check whether GLFW was properly configured on your machine before, download the following code: https://onlinegdb.com/evR9UgF3O

and compile it with

If it compiles properly, then move to the point number 3.



FOR THE FAQ!
If you encountered GLUT (or currently used rewritten FREE GLUT it's very similar toolkit)
