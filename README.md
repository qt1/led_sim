# led_sim
Hardware simulator that enable writing arduino code for led installations even without the hardware

# Setting up codelite and gtkmm

## Ubuntu

### gcc + codelite
Make sure your gcc toolchain is installed. This usually comes with ubuntu at no additional cost.
The following should install a compiler and the gtkmm libraries (lines 1-2).
Then install codelite IDE.
Run the following 5 lines to do all of the above..

```
sudo apt update 
sudo apt install g++ pkg-config libgtkmm-3.0-dev 
sudo apt-key adv --fetch-keys http://repos.codelite.org/CodeLite.asc
sudo apt-add-repository "deb https://repos.codelite.org/ubuntu/ $(lsb_release -sc) universe"
sudo apt install codelite codelite-plugins
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


# Make codelite compile .ino files as c++

Open codelite, go to settings / build settings / compilers / g++

add the file type ino (press new... button on the right of the list) then set:
file type: ino
Handle file as: source
Compilation line: 

```
$(CXX) -xc++ $(SourceSwitch) "$(FileFullPath)" $(CXXFLAGS) $(ObjectSwitch)$(IntermediateDirectory)/$(ObjectName)$(ObjectSuffix) $(IncludePath)
```


