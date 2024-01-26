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
```## Creating our first Gym environment
We've discovered that Gym offers a range of environments for training a reinforcement learning agent. To gain a clear understanding of Gym's environment design, we'll begin with the basic Gym environment. Following that, we'll delve into more complex Gym environments.

# Creating Your First Gym Environment

## Step 1: Install Gym
First, make sure you have Gym installed. If not, you can install it using pip:
```bash
pip install gym
```
## Step 2: Create a New Python File
Create a new Python file for your Gym environment. You can name it whatever you like, such as custom_env.py.
## Step 3: Import Gym and NumPy
In your Python file, import Gym and NumPy:
```
import gym
import numpy as np
```
## Step 4: Define Your Environment Class
Create a class for your custom environment. Your class should inherit from the gym.Env class and implement the required methods: __init__, reset, step, and optionally render.
```
class CustomEnv(gym.Env):
    def __init__(self):
        # Define your environment's parameters here
        pass

    def reset(self):
        # Reset the environment to its initial state and return the initial observation
        pass

    def step(self, action):
        # Take a step in the environment based on the given action and return the next observation, reward, done flag, and additional info
        pass

    def render(self, mode='human'):
        # Render the environment (optional)
        pass
```
## Step 5: Implement the Environment Logic
Inside your __init__ method, you can define any parameters or variables needed for your environment. In the reset method, reset your environment to its initial state and return the initial observation. In the step method, implement the logic for taking a step based on the given action and return the next observation, reward, done flag, and additional info.
## Step 6: Register Your Environment
Register your custom environment with Gym using the gym.make method. This will allow you to create instances of your environment using Gym's standard interface.
```
gym.register(
    id='CustomEnv-v0',
    entry_point='custom_env:CustomEnv',  # Replace 'custom_env' with the name of your Python file
)
```
## Step 7: Test Your Environment
You can now test your custom environment by creating an instance of it and interacting with it using Gym's standard interface:
```
env = gym.make('CustomEnv-v0')
observation = env.reset()
for _ in range(1000):
    action = env.action_space.sample()  # Replace with your own action selection logic
    observation, reward, done, info = env.step(action)
    if done:
        break
env.close()

```





