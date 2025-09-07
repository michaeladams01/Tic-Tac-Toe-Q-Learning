# Tic-Tac-Toe-Q-Learning
This project demonstrates a self‑learning Tic‑Tac‑Toe agent using tabular Q‑learning.
I learned how to build a deep learning neural network, focusing on image recognition, sometimes called computer vision.
It supports both 3^9 and 3^16 boards, where the number of possible states goes up from 3^9 to 3^16. The agent plays million sof games against itself, updating a Q-table to estimate the value of taking certain action in each state. Exploration is controlled by an epsillon=greedy policy that gradually shifts from random play to exploiting learned strategies. 
Key points:
A Q-table is initialized and updated using tha standard Q-learning rule.
Reward signal are +1 for a win, and -1 for a loss and 0 for a draw. Terminal states occur when any row, column or diagonal is filled by the same layer or the board is full.
On the 3x3 board, the agent converges quickly to optimal play, achieving draw rates above 95% and near zero win rates ( since optimal play leads to draw)
On the 4x4 board, learning is slower but still converges to a non-losing strategy; draw probability rises towards 95-100% while win probability drops to zero, reflecting optimal defensive play.
