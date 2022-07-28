a) Maybe you already have gcc installed on your machine?
You can check that by introducing in the command prompt:
![MinGW not found](https://github.com/knitterJ/the-easiest-and-the-fastest-way-to-start-using-OpenGL/blob/main/Windows/1.InstallMinGW/gcc%20and%20g%2B%2B%20not%20found.gif)


If MinGW compiler wasn't found, like in the example above, go to the point b) </br>
Otherwise, go to ![2.GLFW](https://github.com/knitterJ/the-easiest-and-the-fastest-way-to-start-using-OpenGL/tree/main/Windows/2.GLFW) 

b) Download MinGW from the official website
https://osdn.net/projects/mingw/downloads/68260/mingw-get-setup.exe/
The download should start automatically after clicking the link.

c) To facilitate the configuration process, place MinGW directly on your C drive
![MinGWCdrive](https://github.com/knitterJ/the-easiest-and-the-fastest-way-to-start-using-OpenGL/blob/main/Windows/1.InstallMinGW/c.png)

d) You'll need two packages: mingw32-base-bin and mingw32-gcc-g++-bin
![MinGWCorePackages](https://github.com/knitterJ/the-easiest-and-the-fastest-way-to-start-using-OpenGL/blob/main/Windows/1.InstallMinGW/d.png)

e) Add the directory of MinGW (C:\MinGW\bin) to your PATH. 
![PATH](https://github.com/knitterJ/the-easiest-and-the-fastest-way-to-start-using-OpenGL/blob/main/Windows/1.InstallMinGW/e.png)


f) Check in the command prompt, whether MinGW was properly installed and added to the PATH:

![MinGW properly installed](https://github.com/knitterJ/the-easiest-and-the-fastest-way-to-start-using-OpenGL/blob/main/Windows/1.InstallMinGW/gcc%20and%20g%2B%2B%20are%20present%20.gif)
--------------------
WARNING
There's another C++ compiler called mingw-w64, which is built-in to Cygwin. Don't dare to install Cygwin, as the installation process takes  ~10 hours.
