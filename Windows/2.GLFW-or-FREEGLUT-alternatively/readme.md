Next item to configure is GLFW. Based on the official specification:

GLFW is a toolkit, built on top of OpenGL, that handles tasks such as opening an OpenGL window and reading keyboard and mouse input.
So basically, if you want to display a window and see any result, toolkit like GLFW needs to be properly configured. Another very popular toolkit similar to GLFW is Freeglut. Because it's possible to find programs and tutorials with both of them, I wrote tutorial how to configure FreeGlut as well. With the little program that is included to each part, you can test the configuration of each, seperately.
The reason why I explained how to configure the alternative library, is that there are several distributions of the same tools that need to be configured in order to use OpenGL freely. You never know which one you encounter in the tutorials or Github repos. It's definitely good to know how to deal with the 2 most popular ones. List of all toolkits can be found here: https://www.opengl.org/resources/libraries/windowtoolkits/.

But first let's come back to the configuration of GLFW.
a) Download 32-bit Windows binaries from the official GLFW website https://www.glfw.org/download.html and unpack the zip,

b) Go to include folder, copy GLFW and paste it to C:\MinGW\include

c) Next go to lib-mingw folder:
copy glfw3.dll and paste it to C:\MinGW\bin

d) From the same lib-mingw folder:
copy libglfw3dll.a and paste it to C:\MinGW\lib

e) Download the following code: https://onlinegdb.com/evR9UgF3O or copy paste the same code below:
`#include <GLFW/glfw3.h>

int main(void)
{
    GLFWwindow* window;

    /* Initialize the library */
    if (!glfwInit())
        return -1;

    /* Create a windowed mode window and its OpenGL context */
    window = glfwCreateWindow(640, 480, "Hello World", NULL, NULL);
    if (!window)
    {
        glfwTerminate();
        return -1;
    }

    /* Make the window's context current */
    glfwMakeContextCurrent(window);

    /* Loop until the user closes the window */
    while (!glfwWindowShouldClose(window))
    {
        /* Render here */
        glClear(GL_COLOR_BUFFER_BIT);

        /* Swap front and back buffers */
        glfwSwapBuffers(window);

        /* Poll for and process events */
        glfwPollEvents();
    }

    glfwTerminate();
    return 0;
}

`


and compile it with:

`g++ main.cpp -lopengl32 -lglfw3dll`




WARNING! DON'T COMPILE YOUR CODE WITH -lglfw3 like many tutorials indicate, because libglfw3.a is a static library that is not correctly configured for gcc. More to read about it in this Stackoverflow thread: https://stackoverflow.com/questions/22623087/undefined-reference-errors-when-linking-glfw-on-mingw


If it compiles properly, then move to the point number 3.GLAD

If it yields errors check the most common errors in the FAQ below:


FOR THE FAQ...
