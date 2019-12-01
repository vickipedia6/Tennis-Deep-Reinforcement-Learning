# Collaboration and competition

## Learning Algorithm

* The agent is trained using Deep Deterministic Policy Gradient algorithm. Modifications were made to support multiple agents in the tennis environment.
* The sequence of the actor architecture is 
```
INPUT_SIZE = 576

```
```
A Fully Connected Layer with an input size of 576 and activation function leaky Relu 
```
```
A Fully Connected Layer with an input size of 128 and output size of 256 and an activation function Leaky Relu
```
```
A Fully Connected Layer with an input size of 256 and output size of 512 and an activation function Leaky Relu
```
```
A Fully Connected Layer with an input size of 512 and output size of 2 and an activation function tanh
```

* The initial weights are initialized in a uniform distribution

* The sequence of the critic architecture is
```
INPUT_SIZE = 576 
```
```
A Fully Connected Layer with an input size of 576 and activation function Leaky Relu
```
```
A Fully Connected Layer with an input size of 260 (256 plus action size squared) and output size of 256 and an activation function Leaky Relu
```
```
A Fully Connected Layer with an input size of 256 and output size of 1
```

### Hyper parameters

BUFFER_SIZE = int(1e5)  # replay buffer size
BATCH_SIZE = 128        # minibatch size
GAMMA = 0.99            # discount factor
TAU = 1e-3              # for soft update of target parameters
LR_ACTOR = 1e-4         # learning rate of the actor 
LR_CRITIC = 1e-3        # learning rate of the critic
WEIGHT_DECAY = 0        # L2 weight decay

### Plot of Rewards

<img src="/results.png" width=500 px />

* The agent was able to solve the environment in less than 2000 episodes. Initially i tried with 3 FC Layers in Actor architecture but the model didn't converge. So i added another FC layer and tweek the hyperparameters and that did wonders. The agent was able to solve it quickly.

### Training Results 

```
Episode 100    Average Score: 0.000
Episode 200    Average Score: 0.004
Episode 300    Average Score: 0.025
Episode 400    Average Score: 0.009
Episode 500    Average Score: 0.011
Episode 600    Average Score: 0.006
Episode 700    Average Score: 0.009
Episode 800    Average Score: 0.007
Episode 900    Average Score: 0.035
Episode 1000   Average Score: 0.032
Episode 1100   Average Score: 0.065
Episode 1200   Average Score: 0.091
Episode 1300   Average Score: 0.107
Episode 1400   Average Score: 0.146
Episode 1500   Average Score: 0.189
Episode 1600   Average Score: 0.207
Episode 1700   Average Score: 0.272
Episode 1800   Average Score: 0.409
Episode 1900   Average Score: 0.599
Environment solved in 1943 episodes wakanda forever :)

```


### Checkpoints

* Please load the pretrained model using the checkpoints 'actor1.pth','actor2.pth','critic1.pth','critic2.pth'

### Future Ideas 

* I will definitely try to improve this using Proximal Policy Optimization, Asynchronous Actor Critic