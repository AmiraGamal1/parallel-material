# How to run c++ code locally

  **Objective:** <br>

  *   To setup your development environment.
  *	  To compile and run an cpp parallel program.

  **Software:** <br>

  *   MinGW Installation Manager
  *   Visual Studio code

## Installing g++ compiler

1. Visit the website **[MinGW](https://sourceforge.net/projects/mingw/)** and click on Download. MinGW is a native Windows port of the GNU Compiler Collection (GCC), that provide header files and free distributable import libraries for creating native Windows applications.

2. Once the file is downloaded. Open the `mingw-get-setup.exe` file then click on [**Install**]<br>
![MinGW Installation Manager Setup Tool](/image/install_mingw-1.png)

3. I am going to install MinGW under `C:` directory, click on [**continue**]<br>
![MinGW Installation Manager Setup Tool](/image/install_mingw-2.png)

4.	Wait MinGW to install then click on [**continue**]<br>
![MinGW Installation Manager Setup Tool](/image/install_mingw-3.png)

5.	In `MinGW Installation Manager` select `mingw32-base-bin` by clicking on the square control beside the package name. You should see as below <br>
![MinGW Installation Manager Setup Tool](/image/install_mingw-4.png)

6.	Also, you should select all the following package as below<br>
![MinGW Installation Manager Setup Tool](/image/install_mingw-5.png)

7.	On the menu bar, select `Installation` --> `Apply Changes` as shown below<br>
![MinGW Installation Manager Setup Tool](/image/install_mingw-6.png)

8.	Click on the `Apply` as shown below
![MinGW Installation Manager Setup Tool](/image/install_mingw-7.png)

9.	Finally, After the installation finish click on `Close`

10.	After that, go to the installation directory [*in my case* `C:\MinGW\bin`] and copy the directory of the bin folder as shown below<br>
![MinGW Installation directory](/image/install_mingw-9.png)

11.	Go to the setting and write `env` on the search bar, select `Edit environment variables for your account` as shown below<br>
![Windows Setting](/image/install_mingw-10.png)

12.	Select `path` and click on `Edit` as shown below<br>
![Windows Setting](/image/install_mingw-11.png)

13.	Click on `New` to add your copied MinGW path [ *in my case* `C:\MinGW\bin` ]<br>
![Windows Setting](/image/install_mingw-12.png)

14.	Finally click on OK --> OK 


## Installing Visual Studio Code

1. Visit the website **[VS code](https://code.visualstudio.com/Download)** Click on `Windows` to download VS code for Windows, as shown below<br>
![Windows Setting](/image/VScode-1.png)

2. After the download finished open the `VSCodeUserSetup` executable file, when it open select `I accept the agreement` then click on `Next`<br>
![Windows Setting](/image/VScode-2.png)

3.	Select all the option as seen below<br>
![Windows Setting](/image/VScode-3.png)

4.	Finally we are ready to install the VS code, click on `install` and wait untail the setup finish
5.	On the Vs code, on the left-hand side, click on `extension` then in the search bar, write `C++` select `C/C++` and click on `Install` as shown below<br>
![Windows Setting](/image/VScode-10.png)

6.	Close `Vs code`


## Running C++ parallel code on VS code

1.	Right click on the Windows button *or press windows + x* then select *Windows PowerShell Admin* as shown below<br>
![Windows Setting](/image/VScode-5.png)

3.	Navigate to `D:` directory by write `cd d:` as shown below<br>
![Windows Setting](/image/VScode-6.PNG)

4.	Then make directory named `Parallel-codes` [`mkdir Parallel-codes`] as shown below<br>
![Windows Setting](/image/VScode-7.png)

5.	Then navigate to the directory<br>
![Windows Setting](/image/VScode-8.PNG)

6.	Write `code .` to open VS code on the `d:\Parallel-codes` directory
![Windows Setting](/image/VScode-9.PNG)

7.	After `VS code` open, create new file name it `fibo.cpp` and write Fibonacci code in the end of **[Lab(1)](https://khalid-elbadawi.github.io/C425/labs/lab01/)** save `fibo.cpp`,then on the top bar select on `…` --> New Terminal. As shown below<br>
![VS code](/image/VScode-11.png)

8. Before to add `pthread.h` header file you need to install `pthreads` library also known as `POSIX` threads, which is provides a way to create and manage threads in multi-threaded program. To install the library use `mingw-get` command and write `mingw-get install pthreads` on the terminal<br>
![VS code](/image/VScode-12.png)


9. Compile the `fibo.cpp` program. Write this command: `g++ -o fibo -pthread fibo.cpp` on the terminal.<br>
**Let us explain the command in detail:**<br>
  `g++`: GUN Compiler Collection for c++<br>
  `-o fibo`: `-o` flag to create the output file named `fibo`<br>
  `-pthread` flag: tell the compiler to link with the `pthread` library<br>
  `fibo.cpp`: the name of the program<br>
  *Note that: if you want to compile program use `openMP` [add `omp.h` header file]. You need to add [`-fopenmp`] flag [`g++ -o out –fopenmp program.cpp`]*
![VS code](/image/VScode-13.png)


10.	Finally write `./fibo` on the terminal to run `fibo` program<br>
![VS code](/image/VScode-15.png)
