# CSE165 [[Demo video]](https://github.com/Lin-Mao/CSE165/releases/download/0.1/recording.mp4)



[Install virtual machine](#install-virtual-machine)

[Configure virtual machine](#configure-virtual-machine)

[Install dependencies](#install-dependencies)

[Example 1 - Pong](#example-1---pong)

[Example 2 - Rock_Paper_Scissors](#example-2---rock_paper_scissors)


## Install virtual machine

1. Download VirtualBox [[Dowolad link]](https://www.virtualbox.org/wiki/Downloads)

2. Download Ubuntu20.04 image [[Download link]](https://releases.ubuntu.com/20.04.5/)

3. Install ubuntu 20.04 on virtual machine


## Configure virtual machine

### Assign administrative privilege to user
(New user doesn't process administrative privilege.)
```
# Enter administrative mode
su # enter the password set during installing ubuntu 20.04 on virtual machine

gedit /etc/sudoers
```

Edit `/etc/sudoers` by add the following content:
```
# username is set during installing ubuntu 20.04 on virtual machine
# username is cse165 in the demo video
username    ALL=(ALL:ALL) ALL
```
Save and close `/etc/sudoers`.

### Install essential tools
```
# Update apt source first
sudo apt update
```

```
sudo apt install build-essential cmake git 
```

## Install dependencies

* mesa-utils
```
sudo apt-get install mesa-utils
```

* GLUT
```
sudo apt-get install freeglut3-dev
```

* GLFW
```
sudo apt-get install libglfw3-dev
```

* SDL
```
sudo apt-get install libsdl1.2-dev libsdl-mixer1.2-dev libsdl-image1.2-dev libsdl2-dev libsdl2-mixer-dev libsdl2-image-dev
```

* SOIL
```
sudo apt install libsoil-dev libglew-dev
```

## Example 1 - Pong


### Download and compile the code
```
# Download code
wget https://github.com/Lin-Mao/CSE165/releases/download/0.1/Pong.zip

# Unzip package
unzip Pong.zip -d Pong && cd Pong

# Install soil
git clone https://github.com/paralin/soil.git && cd soil

mkdir build && cd build
cmake ..
make

# Install Pong
cd ../../   # return the Pong directory
make    # generate glutapp executable
```

### How to play the game
```
# run the game
./glutapp
```

tips:
* Maxmize the window of the game for better user experience.
* Press space to start the game.
* Use the `W` and `W` key to control the left racket.
* Use the `I` and `K` key to control the left racket.
* Enjoy the game!


## Example 2 - Rock_Paper_Scissors
### Download and compile the code

```
# download code
cd ~ # return home directory
wget https://github.com/Lin-Mao/CSE165/releases/download/0.1/Rock_Paper_Scissors.zip

# unzip package
unzip Rock_Paper_Scissors.zip

# compile code
cd Rock_Paper_Scissors/gameLinux
make # generate main executable
```

### How to play the game
```
# run the game
./main
```

Enjoy the game with the prompts.
