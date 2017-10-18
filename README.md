# An Introduction to Reinforcement Learning

RL lies somewhere in between supervised and unsupervised learning. In supervised learning, one has a labeled dataset where each training sample has a target label. While in unsupervised learning, the dataset is not annotated or labeled. In RL though, one has rewards. Based only on these rewards, the agent learns to conduct itself in the environment. So the idea is one needs some sort of occasional feedback to know whether the agent did the right thing or not and then it can learn from its experiences.

## Concepts :

The following concepts are explained in short to give a quick introduction to RL

* Agent, Environment, State, Action, Reward, Policy and Episode    
      
    A good explanation here : [Demystifying Deep Reinforcement Learning](http://neuro.cs.ut.ee/demystifying-deep-reinforcement-learning/)  
      
    Suppose you are an **agent**, situated in an **environment** (e.g. Breakout game). The environment is in a certain **state** (e.g. location of the paddle, location and direction of the ball, existence of every brick and so on). The agent can perform certain **actions** in the environment (e.g. move the paddle to the left or to the right). These actions *sometimes* result in a **reward** (e.g. increase in score). Actions transform the environment and lead to a new state, where the agent can perform another action, and so on. The rules for how you choose those actions are called **policy**. The environment in general is stochastic, which means the next state may be somewhat random (e.g. when you lose a ball and launch a new one, it goes towards a random direction). The set of states and actions, together with rules for transitioning from one state to another, make up a Markov decision process. One **episode** of this process (e.g. one game) forms a finite sequence of states, actions and rewards.  
      
    The flow is : State -> Action -> Reward -> State -> Action...  
    The episode ends with terminal state.  
      
    Important terms :  
    *Cumulative reward*: The cumulative reward is the discounted sum of reward accumulated throughout an episode.  
    *Policy*: A Policy is the agent’s strategy to choose an action at each state. It is noted by π.  
      
    The **objective** of reinforcement learning is to train an agent such that his policy converges to the theoretical optimal policy.  
      
    More terminologies : http://www-anw.cs.umass.edu/rlr/terms.html  
      
* Policy and Value Functions  
      Value functions (either V or Q) are always conditional on some policy π.  
      **Vπ(s,a)** is the expected return an agent is to receive from being in state s behaving under a policy π(a|s)  
      **Qπ(s,a)** expresses the expected value of first taking action a from state s and then following policy π forever. In other words, it represents the expected return (cumulative discounted reward) an agent is to receive when taking action a in state s, and behaving according to a policy π(a|s)  afterwards (which is the probability of taking an action in a given state).  
  
* RL Algorithms
      The goal of various algorithms is to find an **optimal policy** for an agent.  
      Some algorithms -  
      -  Q-Learning (variants : DQN, Double DQN..)  
      -  SARSA  
      -  Temporal Difference (TD)  
      -  Policy Gradient (Continuous states and actions can be dealt with in exactly the same way as discrete ones, can be used either model-free or model-based as they are a generic formulation)  
      -  Actor Critic, etc.   
              
* Role of neural networks  
* Q-Learning  
* DQN  
* Actor-Critic  
