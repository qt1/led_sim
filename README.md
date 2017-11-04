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
sudo apt ins
