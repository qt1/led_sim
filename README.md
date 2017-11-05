# led_sim
Hardware simulator that enable writing arduino code for led installations even without the hardware

# Setting up codelite and gtkmm

## Ubuntu

### gcc
make sure your gcc toolchain is installed. This usually comes with ubuntu at no additional cost.
The following should install a compiler and the gtkmm libraries :

```
sudo apt update 
sudo apt install g++ pkg-config libgtkmm-3.0-dev 
```

### codelite
install codelite IDE:

```
sudo apt-key adv --fetch-keys http://repos.codelite.org/CodeLite.asc
sudo apt-add-repository "deb https://repos.codelite.org/ubuntu/ $(lsb_release -sc) universe"
sudo apt install codelite
```

## Windows

### MSYS
You'll need an environment for gcc to run and an installer too..

Download and install MSYS according to instructions here:
[http://www.msys2.org/](http://www.msys2.org/)

Note that the instructions request updating the installation befor anything else, so please follow steps 5-7

### gcc & gtkmm
install gcc, tools and gtkmm

```
packman -S mingw-w64-x86_64-gcc  mingw-w64-x86_64-gdb  mingw-w64-x86_64-pkg-config pkg-config  mingw-w64-x86_64-make
packman -S mingw-w64-x86_64-gtkmm3
```

### codelite
install codelite IDE - select windows installer from the codelite download page [https://downloads.codelite.org/](https://downloads.codelite.org/)

Try running some sample code and make sure the compiler, debugger etc are working.


