a) Maybe you already have gcc installed on your machine?
You can check that by introducing in the command prompt:
![MinGW not found](https://github.com/knitterJ/the-easiest-and-the-fastest-way-to-start-using-OpenGL/blob/main/Windows/1.InstallMinGW/gcc%20and%20g%2B%2B%20not%20found.gif)


If MinGW compiler wasn't found like in the example above, go to the point b) (here markup should be placed). Otherwise, go to the point 2.GLFW (here markup should be placed) 

b) Download minGW from the official website
https://osdn.net/projects/mingw/downloads/68260/mingw-get-setup.exe/
The dowload should start automatically

WARNING
There's another dev environment, that contains built-in C++ compiler called Cygwin, but don't dare to install it. The installation process takes  ~10 hours.

c) To facilitate the configuration process, place MinGW directly on your C drive

d) You'll need only these two packages: mingw32-base-bin and mingw32-gcc-g++-bin

e) DO SPRAWDZENIA PONOWNIE NA INNEJ MASZYNCE JAKO, ŻE PRÓBOWAŁEM SPRAWDZAĆ ZAINSTALOWANE GCC KOMENDĄ Z CYGWIN'A
Add the directory of MinGW (C:\MinGW\bin) to your PATH. Please be careful with the capital letters and restart Windows after adding C:\MinGW\bin

f) Check in the command prompt whether MinGW was properly installed and added to the PATH:

![MinGW properly installed](https://github.com/knitterJ/the-easiest-and-the-fastest-way-to-start-using-OpenGL/blob/main/Windows/1.InstallMinGW/gcc%20and%20g%2B%2B%20are%20present%20.gif)

What's interesting OpenGL is already preinstalled in your Windows, but we still need to add two libs.
