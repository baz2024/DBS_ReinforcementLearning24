# A Guide to the Gym Toolkit 
In this tutorial, we will learn about the following topics: 
In this section, we will learn how to install several dependencies that are required for running the code used throughout the book. First, we will learn how to install Anaconda and then we will explore how to install Gym. 
Anaconda is an open-source distribution of Python. It is widely used for scientific computing and processing large volumes of data. It provides an excellent package management environment, and it supports Windows, Mac, and Linux operating systems. Anaconda comes with Python installed, along with popular packages used 

1. Open the Terminal and type the following command to download Anaconda: 
```
wget https://repo.continuum.io/archive/Anaconda3-5.0.1-
Linux-x86_64.sh
```

bash Anaconda3-5.0.1-Linux-x86_64.sh
```	

```
 conda create --name universe python=3.6 anaconda


sudo apt-get update sudo apt-get install golang libcupti-dev libjpeg-turbo8-dev make tmux 
```

```
conda install pip six libgcc swig conda install opencv 
```


```
pip install gym
```

```
git clone https://github.com/openai/gym && cd gym
pip install -e .
```

Just in case, if you get any of the following errors while installing Gym, the following commands will help:

sudo apt-get update sudo apt-get install libgl1-mesa-dev libgl1-mesa-glx libosmesa6.dev python3-pip python3-numpy python3-scipy  
```
``` 
sudo apt-get update
sudo apt-get install python-dev
sudo apt-get install libevent-dev
```
## OpenAI Gym Example
There are plenty of environments for us to play with. As of now, there are 797 environments. Use the following snippet to learn about them
```
import gym
envs = gym.envs.registry.all()
print(envs)
print('Total envs available:', len(envs))
```
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

## Classic control environments
Gym provides environments for several classic control tasks such as Cart-Pole balancing, swinging up an inverted pendulum, mountain car climbing, and so on. Let's understand how to create a Gym environment for a Cart-Pole balancing task. The Cart-Pole environment is shown below:



