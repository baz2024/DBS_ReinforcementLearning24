# A Guide to the Gym Toolkit 
In this tutorial, we will learn about the following topics: • Setting up our machine • Installing Anaconda and Gym • Understanding the Gym environment • Generating an episode in the Gym environment • Exploring more Gym environments • Cart-Pole balancing with the random agent • An agent playing the Tennis game ## Setting up our machine 
In this section, we will learn how to install several dependencies that are required for running the code used throughout the book. First, we will learn how to install Anaconda and then we will explore how to install Gym. ### Installing Anaconda 
Anaconda is an open-source distribution of Python. It is widely used for scientific computing and processing large volumes of data. It provides an excellent package management environment, and it supports Windows, Mac, and Linux operating systems. Anaconda comes with Python installed, along with popular packages used for scientific computing such as NumPy, SciPy, and so on. To download [Anaconda]( https://www.anaconda.com/download/), where you will see an option for downloading Anaconda for different platforms. If you are using Windows or macOS, you can directly download the graphical installer according to your machine architecture and install Anaconda using the graphical installer. 
##### If you are using Linux, follow these steps: 
1. Open the Terminal and type the following command to download Anaconda: 
```
wget https://repo.continuum.io/archive/Anaconda3-5.0.1-
Linux-x86_64.sh
```2. After downloading, we can install Anaconda using the following command: 
```
bash Anaconda3-5.0.1-Linux-x86_64.sh
```	After the successful installation of Anaconda, we need to create a virtual environment. The virtual environment is just an isolated environment for a particular project so that each project can have its own dependencies and will not affect other projects. We will create a virtual environment using the following command and name our environment universe: 

```
 conda create --name universe python=3.6 anaconda```**Note that we use Python version 3.6. Once the virtual environment is created, we can activate it using the following command: **
That's it! Now that we have learned how to install Anaconda and create a virtual environment, in the next section, we will learn how to install Gym. Installing the Gym toolkit Now, install the following dependencies: 
```
sudo apt-get update sudo apt-get install golang libcupti-dev libjpeg-turbo8-dev make tmux htop chromium-browser git cmake zlib1g-dev libjpeg-dev xvfb libav-tools xorg-dev python-opengl libboost-all-dev libsdl2-dev swig 
```

```
conda install pip six libgcc swig conda install opencv 
```
We can install Gym directly using pip. Note that throughout this class, we will use Gym version 0.15.4. We can install Gym using the following command: 

```
pip install gym
```We can also install Gym by cloning the Gym repository as follows: 

```
git clone https://github.com/openai/gym && cd gym
pip install -e .
``` ```

Just in case, if you get any of the following errors while installing Gym, the following commands will help:

sudo apt-get update sudo apt-get install libgl1-mesa-dev libgl1-mesa-glx libosmesa6.dev python3-pip python3-numpy python3-scipy  
``````pip3 install -r requirements.txt sudo python3 setup.py install 
``` •  error: command 'gcc' failed with exit status 1:  ```
sudo apt-get update
sudo apt-get install python-dev
sudo apt-get install libevent-dev
```Now that we have successfully installed Gym.
## OpenAI Gym Example
There are plenty of environments for us to play with. As of now, there are 797 environments. Use the following snippet to learn about them
```
import gym
envs = gym.envs.registry.all()
print(envs)
print('Total envs available:', len(envs))
```