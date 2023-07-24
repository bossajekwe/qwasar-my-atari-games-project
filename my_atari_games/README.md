# Welcome to Atari Games
## Task
TODO - What is the problem? And where is the challenge?
The task in this project is to build a Machine Learning (ML) model that can play perfectly these 3 Atari Games 
- Cartpole Game,
- SpaceInvaders 
- Pacman 
using Reinforcement Learning (RL).

## Description
TODO - How have you solved the problem?
To solve this problem, i have made use of the following packages/modules below;
1. stablebaselines3 for the policy , policy evaluation and other advanced functions to be used in the Reinforcement Learning model.
2. gymnasium for the game environment and other functionalities.
3. PIL or pillow for Image Processing 
4. os module for file handling
5. numpy for numerical computations
6. warnings for filter warnings 

## Installation
TODO - How to install your project? npm install? make? make re?
For one to be able to use this project in this environment, there are no form of installations, however all 
the dependencies (stablebaselines3, gymnasium etc ) must be installed and imported in the local/virtual/cloud machines.

## Usage
TODO - How does it work?
1. I have implemented this model using a class called `DQNAgent`. TO initiate the environment, we can use this
line of code `CartPole_agent = DQNAgent(name = 'CartPole', env_name ='CartPole-v1')`.
Note: the keyword parameters `name` and `env_name` are unique to the Cartpole, SpaceInvaders and Pacman or any
other game. for more information you can check out the official website of gymnasium `https://gymnasium.farama.org/environments/atari/`

2. To test the game randomly to see it that it is working, we use the line of code
`CartPole.play_episodes(num_episodes=10)`.
the value `num_episodes` can assume any value. however, it is advisable you test with any number between 10 and 20
especially for games that are quite complex such as `SpaceInvaders`.

3. To start training the model, we can make use of this line of code 
`CartPole.train(time_steps=100000, stop_value=1000)`
The `time_steps` parameter defines the number of iterations the model should take to learn how to play the 
game. it can assume any non-negative value. it is important to note that for larger values of `time_steps`
the code will also take a longer time to execute.

The `stop_value` is the parameter that is used for `early stopping`. it stops the learning of the game when the 
desired point has been achieved. if the value in the `stop_value`, the learning will take place for the duration
of the specified time.

4. After the model has learnt, we can then evaluate how well the model has learnt using this line of code
`CartPole.evaluate_policy(episodes=10)`
the `episodes` defines the number of episodes for which to evaluate the learned policy on .

5. to predict how the agent will behave we then use this line of code;
`CartPole.play_episodes(num_episodes=10, play_type="predict")`.
this time around we use the same line of code as in 2, but this time we add a second parameter called `play_type`
. We can find out if the agent is making the right decision from the rewards being printed to the standard 
output. This code also generates a video of the gameplay of the agent. The number of episodes specified determines 
the length of the video as it will be combination of the different episodes merged together.

6. To save the model, we can make use of this line of code; `CartPole.save_model(path/to/save)`

7. To load the model, we can use this line of code; `CartPole.load_model(path/to/saved/model)`

8. to close the environment, we can use this line of code; `CartPole.close_env()`.


### The Core Team
Ajekwe Moses Zanzan

<span><i>Made at <a href='https://qwasar.io'>Qwasar SV -- Software Engineering School</a></i></span>
<span><img alt='Qwasar SV -- Software Engineering School's Logo' src='https://storage.googleapis.com/qwasar-public/qwasar-logo_50x50.png' width='20px'></span>
