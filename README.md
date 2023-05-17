TIC TAC TOE
To solve games using AI, we will introduce the concept of a game tree followed by minimax algorithm. The different states of the game are represented by nodes in the  game   tree,  very similar to the above planning problems. The idea is  just  slightly  different.  In the game tree,
 the nodes are arranged  in  levels  that  correspond  to  each player's turns in the game so that 
the  “root”  node  of  the  tree (usually depicted at the top of the diagram) is the      beginning
 position  in  the  game.  In tic-tac-toe, this would be the empty grid with no Xs or Os played
 yet. Under root, on the  second  level,  there  are  the  possible  states that can result from the
 first player’s  moves,  be it X or O. We call  these nodes the “children”    of    the   root node.
Each node on  the  second level,  would  further  have as its children nodes   the   states   that
 can be reached from it by the opposing player's  moves.  This  is  continued,  level  by  level, 
until reaching states where the game is over. In tic-tac-toe, this means that either  one  of  the players gets a line of three and wins, or the board is full and the game ends in a tie.

To solve games using AI, we will introduce the concept of a game tree followed by minimax algorithm. The different states of the game are represented by nodes in the  game   tree,  very similar to the above planning problems. The idea is  just  slightly  different.  In the game tree,
 the nodes are arranged  in  levels  that  correspond  to  each player's turns in the game so that 
the  “root”  node  of  the  tree (usually depicted at the top of the diagram) is the      beginning
 position  in  the  game.  In tic-tac-toe, this would be the empty grid with no Xs or Os played
 yet. Under root, on the  second  level,  there  are  the  possible  states that can result from the
 first player’s  moves,  be it X or O. We call  these nodes the “children”    of    the   root node.
Each node on  the  second level,  would  further  have as its children nodes   the   states   that
 can be reached from it by the opposing player's  moves.  This  is  continued,  level  by  level, 
until reaching states where the game is over. In tic-tac-toe, this means that either  one  of  the players gets a line of three and wins, or the board is full and the game ends in a tie.
ALGORITHM USED:

Minimax algorithm used in artificial intelligence to build a  two player games, such as 
tic-tac-toe, checkers, chess and go. This games are known as zero-sum games, because 
in a mathematical representation: one player wins (+1) and other player loses (-1) or
 both of anyone not to win (0).
The Minimax algorithm is a decision-making algorithm commonly used in game theory
 and artificial intelligence to find toptimal move for a player, assuming that the opponent
 also plays optimally. The algorithm works by  generating  a  game  tree  that   represents 
all  possible moves  and  outcomes  for  both  players. The  algorithm  then  evaluates the 
game tree by assigning  score to each leaf node of the tree,representing the final outcome 
of the game. The score is  assigned based  on  some  heuristic function  that  evaluates the desirability of a particular game outcome for given player.The algorithm then recursively backpropagates the scores up the tree, alternating between minimizing and maximizing 
the score at each level of the tree, representing the turns of the two players. This process 
continues until the root of the tree is reached, which represents the optimal move for the 
player.

The Minimax  algorithm  is  commonly  used  in games such  as chess, checkers, and 
tic-tac-toe, where the game tree is  small  enough to  be   generated and evaluated in a 
reasonable amount of time. However, for larger games such as Go or real-time games 
such as Starcraft, more sophisticated algorithms such as Monte Carlo Tree Search are
 used instead.
