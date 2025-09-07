# Tic-Tac-Toe-Reinforcement Learning
A rough framework of reinforcement learning:
The key interest of reinforcement learning are enviroment, action, reward and state. This can be represented by an analogy in human nature. We perform a number of actions to persue goals, some of them bring us good rewards and others do not. Along the way we keep exploring different paths and try to figure out which action might lead to better rewards utilizing the feedback we get based on our actions to improve out strategies.
For this project I followed the following steps outlined in "An Introduction to Reinforcement Learning Project: Learrning Tic-Tac-Toe via Self-Play Tabular Q-learning" by Ryan Rudes: https://towardsdatascience.com/an-introductory-reinforcement-learning-project-learning-tic-tac-toe-via-self-play-tabular-b8b845e18fe
1. The main premise of the project is a simple RL agent trained to evaluate tic-tac-toe positions in order to return the best moves by playing against itself.
2. Tic-tac-toe, noughts and crosses, or Xs and Os is a paper-and-pencil game for two players who take turns marking the spaces in a three-by-three grid, one with Xs and the other with Os. Tic-tac-toe has 9 squares, therefore there are approximately 3⁹ = 19683 states (and 9 actions, of course). Therefore, we have a table with 19683 x 9 = 177147 cells.
3. 
