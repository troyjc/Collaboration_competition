# Collaboration and Competition
Project #3 for Udacity Deep Reinforcement Learning course.

<figure>
  <video controls="true">
    <source src="tennis.mp4" width="640" height="348" type="video/mp4">
  </video>
</figure>

## Project Details

This project uses the Unity [Tennis](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#tennis) environment.

In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

The task is episodic, and in order to solve the environment, your agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents).

Specifically, after each episode, add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores. This yields a single score for each episode.

The environment is considered solved, when the average (over 100 episodes) of those scores is at least +0.5.

## Getting Started
To set up your python environment to run the code in this repository, follow the instructions below.

1. Create (and activate) a new environment with Python 3.6.

        - __Linux__ or __Mac__:
        ```bash
        conda create --name drlnd python=3.6
        source activate drlnd
        ```
        - __Windows__:
        ```bash
        conda create --name drlnd python=3.6
        activate drlnd
        ```

2. Clone the repository and navigate to the `python/` folder.  Then, install several dependencies.
```bash
git clone https://github.com/udacity/deep-reinforcement-learning.git
cd deep-reinforcement-learning/python
pip install .
```

3. Install the [Progressbar](https://pypi.org/project/progressbar2/) Python package using pip:
```bash
pip install progressbar2
```

4. Download the Tennis environment from one of the links below.  Select the environment that matches your operating system:

  - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
  - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
  - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)


5. Place the file in this directory, and unzip (or decompress) the file.

## Instructions
Running the code in the repository and training the agent is straightforward. The `Tennis.ipynb` Jupyter notebook should be used to run the code in the repository and train the agent.

I trained the policy on a MacBook Pro. The policy is implemented using PyTorch and the model is trained on CPU (only).

The MADDPG algorithm was used to train the policy. See the [report file](file:///Report.pdf) for a detailed description of the model and the training process.
