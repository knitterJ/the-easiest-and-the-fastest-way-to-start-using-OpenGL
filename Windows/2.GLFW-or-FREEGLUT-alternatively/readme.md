## Intro

GLFW is a toolkit, that connects OpenGL with your operating system. It's responsible for the tasks such as opening window or reading keyboard input.
So basically, if you want to display a window to see the result of your code, toolkit like GLFW needs to be properly configured. Another very popular toolkit similar to GLFW is called Freeglut. As you encounter programs and tutorials based on both of them, I also prepared instructions [how to configure Freeglut](https://github.com/knitterJ/the-easiest-way-to-start-using-OpenGL-MinGW-glfw-or-freeglut-glad-or-glew-no-cmake/tree/main/Windows/FREEGLUT). So if your code contains `include <GL/glut.h>` or `include <GL/freeglut.h>` go directly to the link above. 

## How to configure GLFW

a) Download 32-bit Windows binaries from the official GLFW website https://www.glfw.org/download.html and unpack the zip (no matter whether you have 64 or 32-bit Windows),

b) Go to include folder, copy GLFW and paste it to `C:\MinGW\include`

![](https://github.com/knitterJ/the-easiest-way-to-start-using-OpenGL-MinGW-glfw-or-freeglut-glad-or-glew-no-cmake/blob/main/Windows/2.GLFW-or-FREEGLUT-alternatively/b2.gif)

c) Next go to lib-mingw folder:
copy glfw3.dll and paste it to `C:\MinGW\bin`

![](https://github.com/knitterJ/the-easiest-way-to-start-using-OpenGL-MinGW-glfw-or-freeglut-glad-or-glew-no-cmake/blob/main/Windows/2.GLFW-or-FREEGLUT-alternatively/c.png)

d) From the same lib-mingw folder:
copy libglfw3dll.a and paste it to `C:\MinGW\lib`

![](https://github.com/knitterJ/the-easiest-way-to-start-using-OpenGL-MinGW-glfw-or-freeglut-glad-or-glew-no-cmake/blob/main/Windows/2.GLFW-or-FREEGLUT-alternatively/d.png)

e) Download the following code: https://onlinegdb.com/evR9UgF3O or copy paste the same code below:

```
#include <GLFW/glfw3.h>

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

```


and compile it with:

`g++ main.cpp -lopengl32 -lglfw3dll`


WARNING! DON'T COMPILE YOUR CODE WITH -lglfw3 like many tutorials indicate, because libglfw3.a is a static library that is not correctly configured for gcc environment. More in this Stackoverflow thread: https://stackoverflow.com/questions/22623087/undefined-reference-errors-when-linking-glfw-on-mingw

![](https://github.com/knitterJ/the-easiest-way-to-start-using-OpenGL-MinGW-glfw-or-freeglut-glad-or-glew-no-cmake/blob/main/Windows/2.GLFW-or-FREEGLUT-alternatively/f.png)

f) If it compiles properly, then move to [3.GLAD](https://github.com/knitterJ/the-easiest-way-to-start-using-OpenGL-MinGW-glfw-or-freeglut-glad-or-glew-no-cmake/tree/main/Windows/3.GLAD-or-GLEW-alternatively)

