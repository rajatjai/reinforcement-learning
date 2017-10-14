# An Introduction to Reinforcement Learning

RL lies somewhere in between supervised and unsupervised learning. In supervised learning, one has a labeled dataset where each training sample has a target label. While in unsupervised learning, the dataset is not annotated or labeled. In RL though, one has rewards. Based only on these rewards, the agent learns to conduct itself in the environment. So the idea is one needs some sort of occasional feedback to know whether the agent did the right thing or not and then it can learn from its experiences.

Concepts :

The following concepts are explained in short to give a quick introduction to RL

* Agent, Environment, State, Action, Reward, Policy and Episode    
      
    A good explanation here : [Demystifying Deep Reinforcement Learning](http://neuro.cs.ut.ee/demystifying-deep-reinforcement-learning/)  
      
    Suppose you are an **agent**, situated in an **environment** (e.g. Breakout game). The environment is in a certain **state** (e.g. location of the paddle, location and direction of the ball, existence of every brick and so on). The agent can perform certain **actions** in the environment (e.g. move the paddle to the left or to the right). These actions *sometimes* result in a **reward** (e.g. increase in score). Actions transform the environment and lead to a new state, where the agent can perform another action, and so on. The rules for how you choose those actions are called **policy**. The environment in general is stochastic, which means the next state may be somewhat random (e.g. when you lose a ball and launch a new one, it goes towards a random direction). The set of states and actions, together with rules for transitioning from one state to another, make up a Markov decision process. One **episode** of this process (e.g. one game) forms a finite sequence of states, actions and rewards.  
      
    The flow is : State -> Action -> Reward -> State -> Action...  
    The episode ends with terminal state.  
      
* Role of neural networks  
* Q-Learning  
* DQN  
* Policy and Value Functions  
* Actor-Critic  
