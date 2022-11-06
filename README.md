# CSE165

## Install virtual box

## Install ubuntu 20.04 on virtual machine

## Example - Pong

### Install dependencies

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
sudo apt-get install libsdl1.2-dev libsdl-mixer1.2-dev libsdl-image1.2-dev
sudo apt-get install libsdl2-dev libsdl2-mixer-dev libsdl2-image-dev
```

### Download and install code
```
# Download code
wget https://github.com/Lin-Mao/CSE165/releases/download/0.1/Pong.zip

# Unzip package
unzip Pong.zip -d Pong

# Install soil
git clone https://github.com/paralin/soil.git && cd soil

mkdir build && cd build
cmake ..
make

# Install Pong
cd ../../   # return the Pong directory
make    # generate glutapp executable file
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

