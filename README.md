# Tic-Tac-Toe-Reinforcement Learning
A rough framework of reinforcement learning:
The key interest of reinforcement learning are enviroment, action, reward and state. This can be represented by an analogy in human nature. We perform a number of actions to persue goals, some of them bring us good rewards and others do not. Along the way we keep exploring different paths and try to figure out which action might lead to better rewards utilizing the feedback we get based on our actions to improve out strategies.
For this project I followed the following steps outlined in "An Introduction to Reinforcement Learning Project: Learrning Tic-Tac-Toe via Self-Play Tabular Q-learning" by Ryan Rudes: https://towardsdatascience.com/an-introductory-reinforcement-learning-project-learning-tic-tac-toe-via-self-play-tabular-b8b845e18fe
1. The main premise of the project is a simple RL agent trained to evaluate tic-tac-toe positions in order to return the best moves by playing against itself.
2. Tic-tac-toe, noughts and crosses, or Xs and Os is a paper-and-pencil game for two players who take turns marking the spaces in a three-by-three grid, one with Xs and the other with Os. Tic-tac-toe has 9 squares, therefore there are approximately 3⁹ = 19683 states (and 9 actions, of course). Therefore, we have a table with 19683 x 9 = 177147 cells.
### Initialize q-table of shape (states, actions), which is (3 ** 9, 9)
q_table = np.zeros((3 ** 9, 9))
### Learning parameters
episodes = 1000000
learning_rate = 0.01
num_random_episodes = 10000
min_epsilon, max_epsilon = 0.01, 1.0
### Epsilon decay function
The Epsilon decay function sets up a exploration-explotation strategy where the epsilon value starts high (favoring eploration) and gradualy decreses over episodes (favoring exploitation) until it reaches a minimum value.
def get_epsilon(episode):
  epsilon = max(min_epsilon, min(max_epsilon, num_random_episodes / (episode + 1)))
  return epsilon
### Show graph of exploration strategy
This code visualizes the exploration strategy used in the reinforcement learning algorithm. It generates a plot showing how the epsilon value (which determines the probability of taking a random action) changes over the course of the training episodes.
### Get available moves
In tic-tac-toe occupied squares are no longer available, so we need a funtion to return legal moves
