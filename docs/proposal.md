## Summary of the Project

We are aiming to design a simple game like "Subway Surfer" in Minecraft. Given a starting point and an ending line, The goal of agent is keep going forward while jumping or moving right or left to avoid obstacles and getting as much gold as possible. We will first using randomized function to generate random obstacles(lava, blocks etc), gold on the map. Then, the function will choose a starting point and an ending line for the agent to reach. Our algorithm will take the position of the agent and the the structure of the map as inputs and the agent's track to the ending line as the output. By doing reinforcement learning, the output will start by being a randomized track which might encounter obstacles. Then, after training for a while, the output will be an artful track which dodged obstacles and got as much gold as possible.

## AI/ML Algorithm

In this project, we plan to use Q-Learning algorithm under Reinforcement Learning. 


## Evaluation Plan

### Quantitative: 
We will evaluate the success by adding the Q-value for each state and action pair. Rewarding scheme for different actions will be used to calculate the final Q-value. For example, the agent will get +0 reward when staying static (including jump in place) and getting +1 reward when moving one step forward towards the end. A Q table will be initialized as 0 for n rows (n=number of states) and m cols (m=number of actions). This table will be used to keep storing and updating Q-values for each pair. To calculate Q-value, we will use the Bellman equation with each action and state pair as input. 

$$ q^{new}\left( s,a\right) =\left( 1-\alpha \right) ~\underset{\text{old value} }{\underbrace{q\left( s,a\right) }\rule[-0.05in]{0in}{0.2in} \rule[-0.05in]{0in}{0.2in}\rule[-0.1in]{0in}{0.3in}}+\alpha \overset{\text{ learned value}}{\overbrace{\left(R_{t+1}+\gamma \max_{a^{^{\prime }}}q\left( s^{\prime },a^{\prime }\right) \right) }} $$

At the beginning, we will set the epsilon greedy strategy as 1 to ask our agent explore the enviornment with random actions. With more information being learned, the epsilon will be decreased accordingly, which enables our agent to both explore and exploit with knowledge in the environment. 

### Qualitative:
The ideal situation after being trained is that our agent can reach the end point by learning how to avoid obstables and collecting as much as gold as possible. Our agent should be able to identify obstacles and gold. Our agent will understand under which situation he will lose points and result in game over, and how he can reach the end points with more positive rewards. 

## Apointment

9:45am - 10:00am, Thursday, October 22, 2020
