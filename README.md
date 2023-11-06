# Reinforcement-Learning-with-SARSA
How to teach an intelligent agent to play simple games using State-Action-Reward-State-Action (SARSA) algorithm. 

SARSA is a value-based method similar to Q-learning. Hence, it uses a Q-table to store values for each state-action pair. With value-based strategies, we train the agent indirectly by teaching it to identify which states (or state-action pairs) are more valuable.

Typically we start with all values in a Q-table initialized to 0, and we use training to optimize the Q-table. Then our agent can use information stored in a Q-table to choose the best action at each state (i.e., the action with the highest value for each state is the one selected by the agent).

SARSA is an on-policy algorithm, which is one of the areas differentiating it from Q-Learning (off-policy algorithm). On-policy means that during training, we use the same policy for the agent to act (acting policy) and to update the value function (updating policy). Meanwhile, with the off-policy approach, we use different policies for acting and updating.

Now let’s take a look at the SARSA algorithm itself:

𝑄(𝑆𝑡,𝐴𝑡)=𝑄(𝑆𝑡,𝐴𝑡)+𝛼[𝑅𝑡+1+𝛾𝑄(𝑆𝑡+1,𝐴𝑡+1)−𝑄(𝑆𝑡,𝐴𝑡)]

Since SARSA uses Temporal Difference (TD) approach, the algorithm will keep updating the Q-table after each step until we reach the maximum number of iterations or the solution converges to an optimal one.

Comparison to Q-Learning: 

If we look at the equation used by the Q-Learning algorithm, we can see that the difference lies in how it selects the value of the next state. I.e., Q-Learning takes the maximum value for the next state based on the existing values in the Q-table. Meanwhile, SARSA takes the value of the next state-next action pair, as seen above.

If we look at the equation used by the Q-Learning algorithm, we can see that the difference lies in how it selects the value of the next state. I.e., Q-Learning takes the maximum value for the next state based on the existing values in the Q-table. Meanwhile, SARSA takes the value of the next state-next action pair, as seen above. Since it is an on-policy algorithm. 

Q-Value Formula: 

𝑄(𝑆𝑡,𝐴𝑡)=𝑄(𝑆𝑡,𝐴𝑡)+𝛼[𝑅𝑡+1+𝛾MAX𝑄(𝑆𝑡+1,𝐴𝑡+1)−𝑄(𝑆𝑡,𝐴𝑡)]

Value-based RL like Q-Learning, SARSA, or DQN are best suited when the action space is discrete and not too large.




