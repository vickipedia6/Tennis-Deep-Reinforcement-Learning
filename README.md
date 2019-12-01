# Tennis-Deep-Reinforcement-Learning

In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

The task is episodic, and in order to solve the environment, your agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,

* After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.This yields a single score for each episode.

Solution : 

The environment is considered solved, when the average (over 100 episodes) of those scores is at least +0.5.

## Getting Started

### Download the Unity Environment

For this project, you will not need to install Unity - this is because we have already built the environment for you, and you can download it from one of the links below. You need only select the environment that matches your operating system:

* Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
* Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
* Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
* Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)

Then, place the file in the folder in the Tennis-Deep-Reinforcement-Learning GitHub repository, and unzip (or decompress) the file.

### Output

<img src="/out.gif" width= 500 px/>

### Instructions

 1. Download the project materials from my GitHub repository. You can download the repository with
  ```
  git clone https://github.com/vickipedia6/Tennis-Deep-Reinforcement-Learning.git
  ```
 2. Download anaconda or miniconda based on the instructions in the [Anaconda documentation](https://docs.anaconda.com).
 
 3. Create a new conda environment:
  ```
  conda create --name deep-learning python=3
  ```
 4. Enter your new environment:
  * Mac/Linux: >> ``` source activate deep-learning ```
  * Windows: >>  ```activate deep-learning ```
  
 5. Ensure you have numpy, matplotlib, pandas, and jupyter notebook installed by doing the following:
  ```
  conda install numpy matplotlib pandas jupyter notebook
  ```
 6. Run the following to open up the notebook server:
  ```
  jupyter notebook Tennis.ipynb
  ```
 7. Execute all the cells in the code
 
### Project results

* The agent achieved the average score of 0.7 in less than 2000 episodes.

<img src="/results.png" width= 700 px/>

## Built With

* Python 3

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* The data comes from the Udacity.

