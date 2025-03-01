# Artificial Intelligence A-Z: Learn How To Build An AI - Notes


## Table Of Contents

  - [Section 1: Welcome to the course](#section-1-welcome-to-the-course)
    - [1. Why AI ?](#1-why-ai-)
    - [2. Course structure : OK](#2-course-structure--ok)
    - [4. Anaconda installation : OK](#4-anaconda-installation--ok)
    - [5. Extra Materials : sdsclub.com/artificial-intelligence-a-z-learn-how-to-build-an-ai](#5-extra-materials--sdsclubcomartificial-intelligence-a-z-learn-how-to-build-an-ai)
  - [Section 2: - Part 0 - Fundamentals Of Reinforcement Learning](#section-2---part-0---fundamentals-of-reinforcement-learning)
    - [6. the problem setup :](#6-the-problem-setup-)
  - [Section 3: Q-Learning intuition](#section-3-q-learning-intuition)
    - [7. plan of attack](#7-plan-of-attack)
    - [8. What is reinforcement learning ?](#8-what-is-reinforcement-learning-)
    - [9. The Bellman Equation](#9-the-bellman-equation)
    - [10. The "Plan"](#10-the-plan)
    - [11. Markov Decision Process (MDP)](#11-markov-decision-process-mdp)
    - [12. Policy vs Plan](#12-policy-vs-plan)
    - [13. Living Penalty](#13-living-penalty)
    - [14. Q-Learning intuition](#14-q-learning-intuition)
    - [15. Temporal Difference](#15-temporal-difference)
  - [Section 4: Q-Learning Visualization](#section-4-q-learning-visualization)
    - [16. Gridworld set up](#16-gridworld-set-up)
    - [17. Q-Learning Visualization](#17-q-learning-visualization)
  - [Section 5: - Part 1 - Deep Q-Learning](#section-5---part-1---deep-q-learning)
    - [18. Intro part 1](#18-intro-part-1)
  - [Section 6: Deep Q-Learning Intuition](#section-6-deep-q-learning-intuition)
    - [19. Plan of attack](#19-plan-of-attack)
    - [20. Deep Q-Learning Intuition (Learning)](#20-deep-q-learning-intuition-learning)
    - [21. Deep Q-Learning Intuition (Acting)](#21-deep-q-learning-intuition-acting)
    - [22. Experience Replay](#22-experience-replay)
    - [23. Action Selection Policies](#23-action-selection-policies)
  - [Section 7: Deep Q-Learning Implementation](#section-7-deep-q-learning-implementation)
    - [24. Plan of Attack](#24-plan-of-attack)
    - [25. Project resources](#25-project-resources)
    - [26. Getting started](#26-getting-started)
  - [Section 8: Deep Q-Learning Visualization](#section-8-deep-q-learning-visualization)
    - [43. Self-Driving Car - Level 1](#43-self-driving-car---level-1)
    - [44. Self-Driving Car - Level 2](#44-self-driving-car---level-2)
    - [45. Self-Driving Car - Level 3](#45-self-driving-car---level-3)
    - [46. Self-Driving Car - Level 4](#46-self-driving-car---level-4)
    - [47. Challenges Solutions](#47-challenges-solutions)
  - [Section 9:  Part 2 - Deep Convolutional Q-Learning](#section-9--part-2---deep-convolutional-q-learning)
    - [48. Welcome to Part 2 - Deep Convolutional Q-Learning](#48-welcome-to-part-2---deep-convolutional-q-learning)
  - [Section 10: Deep Convolutional Q-Learning Intuition](#section-10-deep-convolutional-q-learning-intuition)
    - [49. Plan of Attack](#49-plan-of-attack)
    - [50. Deep Convolutional Q-Learning Intuition](#50-deep-convolutional-q-learning-intuition)
    - [51. Eligibility trace](#51-eligibility-trace)
  - [Section 11: Deep Convolutional Q-Learning Implementation](#section-11-deep-convolutional-q-learning-implementation)
    - [52. Plan of Attack](#52-plan-of-attack)
    - [54. to 69 : Deep Q-Learning Implementation for game of Doom](#54-to-69--deep-q-learning-implementation-for-game-of-doom)
  - [Section 12: Deep Convolutional Q-Learning Visualization](#section-12-deep-convolutional-q-learning-visualization)
    - [69 - 73](#69---73)
  - [Section 13: - Part 3 - A3C](#section-13---part-3---a3c)
    - [74. Welcome to Part3 - A3C](#74-welcome-to-part3---a3c)
  - [Section 14: A3C Intuition](#section-14-a3c-intuition)
    - [75. Plan of Attack](#75-plan-of-attack)
    - [76. The 3 A's of A3C](#76-the-3-as-of-a3c)
    - [77. Actor-Critic](#77-actor-critic)
    - [78. Asynchronous](#78-asynchronous)
    - [79. Advantage](#79-advantage)
    - [80. Long Short-Term Memory (LSTM)](#80-long-short-term-memory-lstm)
  - [Section 15: A3C Implementation](#section-15-a3c-implementation)
    - [81 to 96](#81-to-96)
  - [Section 16: ASC Visualization](#section-16-asc-visualization)
    - [97 - 98](#97---98)
  - [Section 17: Annex 1: Artificial Neural Networks](#section-17-annex-1-artificial-neural-networks)
  - [Section 18: Annex 2: Convolutional Neural Networks](#section-18-annex-2-convolutional-neural-networks)
  - [Section 19: Bonus Lectures](#section-19-bonus-lectures)
    - [124. YOUR SPECIAL BONUS](#124-your-special-bonus)
- [References :](#references-)


## Section 1: Welcome to the course  

### 1. Why AI ? 
- It's the best time to be in AI ! 
- Applications : Self-driving cars, medicine, heavy machanery, customer service ...
- Moore's Law : computer power will double every 2yrs 
    - Strategy games :
        - Chess : DeepMind vs Gary Kasparov (1997)
        - Go : AlphaGo vs Lee Sedol (2016)
- Game to train AI : confined environment then apply that to solve the real world problems/business

### 2. Course structure : OK
- course resources & code template :  https://www.tfcertification.com/pages/artificial-intelligence
- 2.1 BONUS - Learning Paths :  https://sdsclub.com/learning-paths/ai-engineer/
### 4. Anaconda installation : OK 
### 5. Extra Materials : sdsclub.com/artificial-intelligence-a-z-learn-how-to-build-an-ai
    5.1 - QA : https://datascience.stackexchange.com/
    5.2 - To Becoming A Better Data Scientist  : interaction & feedbacks, help others, debugging, purpose ...
    5.3 - Discord for feedback 

## Section 2: - Part 0 - Fundamentals Of Reinforcement Learning

### 6. the problem setup :

How humans learn ? 
- The thing is we already know how we, humans, learn. 
- We understand the concepts of intrinsic and extrinsic rewards that guide us to become better at things. 
- For example, if you're playing bowling - you know that you need to hit the pins and a strike is a perfect shot.
- We know this because we are rewarded with points for hitting the pins down and we are "punished" with no points when your ball ends in the ditch. 
- So your brain projects those conditions of the environment onto your actions and that's how you know when you are doing good and when - not so much. 
- And that's how we learn.

How AI learns ? 
- But how do we explain that to an Al? 
    - Reinforcement Learning : learning processes similar Conceptually to human  

## Section 3: Q-Learning intuition

### 7. plan of attack

What we will learn in this section: 
- What is Reinforcement Learning? 
- The Bellman Equation 
- The "Plan" 
- Markov Decision Process (MDP) 
- Policy vs Plan 
- Adding a "Living Penalty" 
- Q-Learning Intuition 
- Temporal Difference 

### 8. What is reinforcement learning ?

Model : 
- Environment : the state of environment will change, it will also get a reward based on the actions taken by the agent
- Agent : performs action in the environment
- the number of iterations enable the Angent to learn about its environment and optimize which actions lead to bad rewards and unfavorable states 
- actions should be taken at the correct points in time (sequentual ? one after anoter ?)   
- reward : +1 for good action  ou -1 bad action/command 

- Ex of ai learning process : training a robotdog how to walk

Pre-programmed learning vs reinforcement learning 
- pre-programmed learning :  actions are programed in advance (move forward, left, right ...)
- reinforcement learning : there is no an hard-coded algorithm into the dog, there is a reinforcement model 
    - move towards a specific target, it gets a reward (+1/-1)
    - throught repetition it undertands how it can walk 
    - by numerous iteration it can optimize things on it own and  we get a better results 

- Addictional reading : 
    - [research paper by Richard Sutton et al. (1998)](http://citeseer.ist.psu.edu/viewdoc/summary?doi=10.1.1.32.7692)

### 9. The Bellman Equation

Invented by Richard Ernest Bellman, a Mathematician who came up w/ the Dynamic programing concept (today called RL) in 1953

Concepts : 
- s - State (where the agent is )
- a - Action (taken by the agent)
- R - Reward (got by the agent for entering into a certain state)
- Y(gamma) - Discount factor

Actions/List of actions are often associated with states.

How it works ? 

|      |       |       |Target | 
|------|-------|-------|-------|
|      |       |       |  Fire |
|      |   X   |       |       |
|   A  |       |       |       |

if A get reach the target => R = +1
If A == X => R=-1 
If A == Fire => R=-1 

each time the Agend(A) takes an action the state also change. 
The challenge is to make the Agent take the actions that lead to a positive reward based on previous states results(valuables state). 

How to calculate Valuable States (V)? 
- the idea is to go a backward from the target where a R=+1 and create pathway to the starting point. Then, detect every adjacent square or state that lead to target and value it V=1, and repeat the process until the full path is recreated from the starting point.
- Build the equation that helps the agent go through the maze:
    - look at reward, then the preceding state give a value of equal reward and so on to create a pathway.
    - the problem with approach is that if the Agent starts from any other state than the starting point it doesnot know anymore how to reach the target(Reward)

**Solution : dynamique programming the Bellman Equation**

    V(s) = max[R(s, a) + Y*V(s')]

where : s' - the next/future state
- Y : solve the situation where the agent doesn't know which way to go.
- The value of Y is chosen under certain conditions(ex: 0.9)
- Also we calculate the maximum value in each state until the starting point. 
- The pattern is that the preceding state < than the actual state. The closer you are to the finish line the more valuable that state is.
- With this concept it's easier to know which direction the agent must go.

### 10. The "Plan"

- create a navigation map of AI.
- we can replace the state value with the arrow indicating the direction to the finish line
- plan different from "policy"

### 11. Markov Decision Process (MDP)

The navigation map is not that simple that's where MDP comes to play.

- Deterministic search : always produce the same output from a given starting condition or initial state (ex : if the agent is told to go up there's a probability of 100% it goes in this direction)
- Non-deterministic search(stochastic process) : multiple possible outcomes from a given starting condition or initial state (ex : if the agent is told to go up there's a probability of 80% it goes up, 10% left or 10% right)  
    - How randomness affects an environment and how to deal w/ it 
    - Using Markov Decision Process

What's Markov Process ?
>A stochastic process has the Markov property if the conditional probability distribution of future states of the process (conditional on both past and present states) depends only upon the present state. not on the sequence of events that preceded it. A process with this property is called a **Markov process** (src : wikipedia)

What's Markov Decision Processes?
> Markov Decision Processes (MDPs) provide a mathematical framework for modeling decision making in situations where outcomes are partly random and partly under the control of a decision maker.(src: wikipedia)

- A MDP is a version of Bellman equation but sophisticated

        V(s) = max[R(s, a) + Y*Sum(P(s,a, s')*V(s'))]

where : 
- P(s,a,s') : is the Probability of the action to go the actual state to a future state
- Sum : sum of the probability of different actions available for every new state possibility
- s' : the new/future state

Addictional resources :
- A survey of Applications of Markov Decision Processes by D. J. White(1993)
- Link : http://www.it.uu.se/edu/course/homepage/aism/st11/MDPApplications3.pdf

### 12. Policy vs Plan

- Policy : Applied in the non-deterministic world also known as Stochastic (random signals/ unpredictable events in the system)
    - the agent can have more than one action to execute in the same state based on the number of possibilities(probabilities)
    - then if the next state has a value of 0% or -1 reward we move onto the next state/obstacle based on the other neighbour state  
    - due to the randomness we can see a same action executed in different states  

- Plan : when you know what you need to do next (predictible actions)
    - We take the value of value function straghtforward compares if is less than current reward to move back/forward (create a plan)

### 13. Living Penalty
- Negative reward or the probability to get a reward (-1)
- build a strategy to check when the agent reach a negative reward 
- the bigger the value(closed to -1) the more the agent will get straight to the negative reward state
- The reward is given in every given states

### 14. Q-Learning intuition
- V(s) represents the value of the action
- Q(s,a) represents the quality of the action
- a state can have multiple actions
- actions leads to (future)states

        Q(s,a) = R(s, a) + Y*Sum(P(s,a, s')*V(s'))

then, 

        V(s) = max(Q(s,a)) => V function is the maximum of all of possible Q-values
Normalizing according to Q-value : 

        Q(s,a) = R(s, a) + Y*Sum[P(s,a, s')*max(Q(s', a'))]

Additionnal resources : 
- Markov Decision Processes : Concepts and algorithms by Martijn van Otterlo(2009) 
    - Link : http://pdfs.semanticscholar.org/968b/ab78e52faf0f7957ca0f38b9e9078454afe.pdf

### 15. Temporal Difference
- the heart and soul of Q-learning intuition
- mechanism which allows the agent to calculate the probability values(V-values) during the each state
- How the Q-value is updates 

Q-value in a determinist forme : 

    Q(s,a) = R(s, a) + Y*max(Q(s', a'))

Temporal difference :

    TD(s,a) =  R(s, a) + Y*max(Q(s', a')) - Q(s,a)

 where : (current Q-value minus previous Q-value) // (future Q-value minus the current Q-value) 
- the computation occurs every t time iteration

        Qt(s,a) =  Qt-1(s,a) + alpha*TDt(s,a)

- where *alpha* is the learning rate(how quick the algorithm is learning)

        Qt(s,a) =  Qt-1(s,a) + alpha*[R(s, a) + Y*max(Q(s', a')) - Qt-1(s,a)]
- if *alpha* = 0, **Qt(s,a) =  Qt-1(s,a)** no learning is done

Additional resources : 
- Learning to predict by the Methods of temporal Differences by Richard Sutton (1998)

## Section 4: Q-Learning Visualization

### 16. Gridworld set up
- Reinforcement learning project with code from Berkeley University, California 
    - Link : http://ai.berkeley.edu/reinforcement.html 
### 17. Q-Learning Visualization 
- AI course & projects 
    - link :  http://ai.berkeley.edu/home.html
- UC Berkeley Lab : 
    - lab : https://bair.berkeley.edu/


## Section 5: - Part 1 - Deep Q-Learning
### 18. Intro part 1 
- Deep Q-Learning = Q-Learning + Artificial Neural Network
- Self-driving cars application 
## Section 6: Deep Q-Learning Intuition
### 19. Plan of attack 
- Deep Q-Learning Intuition (Learning)
- Deep Q-Learning Intuition (Acting)
- Experience Replay
- Action Selection Policies
### 20. Deep Q-Learning Intuition (Learning)
- Q-learning + deep learning
- for more complex environments like self-driving cars
- a state in now represented as a pair input values (x1, x2)
- deep learning predicts the future Q(s,a) value by comparing with previous predicted target
    - Qx - Qtarget(estimator) = newQ
    - we adjust the weights of NN to get a better result

Loss function of NN:

    L (mse) = Sum(Qtarget - Q)^2

why not cross-entropy ? 

- we want the loss to be small as possible(close to zero ? ) by using backprogagation(updates weight & bias) during fitting with gradient descent 
    - Optmizer : Gradient descent (derivative of L)

### 21. Deep Q-Learning Intuition (Acting)
- output of the deep NN (Q) is passed to a softmax function for prediction
- a Softmax function(a generalization form of sigmoid) the highest score gets is passed to output and gets the highest propability(%)
- Softmax calculate the best action possible

### 22. Experience Replay
- in the case of a self-driving car
    - the state is the steering angle, speed, throtle...
    - every time the the car ends up in a new state NN inputs states gets updated this causes dependency btw old state and new one and correlation
- Unstable learning issues due to high correlation in the input sequence data(large number of samples)
- Experience replay :  stores past experience in memory and use these samples during the learning stage or every time step *t* (iteration) to reduce correlation of sequence of data and avoiding overffiting  
- saves different experiences in a batch and then reused them whenever we want 

additional reading : 
    - Prioritized Experience replay : Tom Schaul et al - DeepMind (2016) 
    - link : https://arxiv.org/pdf/1511.05952.pdf

### 23. Action Selection Policies
- we have different action selection because of **Exploration** vs **Exploitation** problems
- a good/great action can produce a bad reward (-1) then all the network as to be revaluated again to provide even a better action therefore a bette reward(+1)=> Policy!!!
- most common *action selection* : 
    - epslon-greedy : selects the action with the best Q-value all time exception epslon(e)% of the time => ex : (Q-value 95% and e = 5% random action => if value > e -> good action, bad action otherwise )
    - epslon-soft(1-e) : opposite of epslon-greedy  
    - Softmax : selects the highest action possible, the higher the Q-value the best the action 


Additional reading: 
- Adaptive e-greedy Exploration in Reinforcement Learning Based on Value differences by Michel tokic (2010)

## Section 7: Deep Q-Learning Implementation
### 24. Plan of Attack
- In this Module we are going to build a Self Driving Car... from scratch !
1. First, we will build the environment containing the map, the car and all the features that go with it.
2. Then, we will build the AI, which will be the Deep Q-Learning model.
3. And eventually, we will have our exciting demo. 
### 25. Project resources
ok
### 26. Getting started
from #27 to #42 Implementation/demo : 
link : https://github.com/afondiel/my-lab/tree/master/automotive/self-driving-cars/project/self-driving-car-rl

## Section 8: Deep Q-Learning Visualization
### 43. Self-Driving Car - Level 1
- Going from A to B destination 
  - example : DOWNTOWN(A) to the AEROPORT(B)
  - then we save the model
    - In the beginning the Agent is exploring the env and learning through punishements(negative reward) then when it finally learn, it gets positive rewards   
### 44. Self-Driving Car - Level 2
- A drawn road : 
  - Straight road with lane in both sides and the car shall be able to stay on the track between the lanes
### 45. Self-Driving Car - Level 3

- A drawn road + Obstacles : 
  - same goal as the level 2 but with some obstacles in the road and the car has to be able to avoid them

### 46. Self-Driving Car - Level 4
- Challenge road : zigzag shape, ... and yet the car has to be able to reach its goal
### 47. Challenges Solutions
**Problem setup :** 
- when the car goes way from the goal, the error/punishment increase and it get stuck. The idea is to pusnish less when the car get further from the goal
  
*Improvements tips  :* 
  - change NN
  - change game strategy
  - Q-learning algo  ? find a better one
  - change reward computing  strategy ... 
  - try different graphs (high-ways, traffic-circle, intersection...parking lot )
  
## Section 9:  Part 2 - Deep Convolutional Q-Learning
### 48. Welcome to Part 2 - Deep Convolutional Q-Learning
- Ok 
## Section 10: Deep Convolutional Q-Learning Intuition
### 49. Plan of Attack
- Deep Convolution Q-Learning Intuition
- Eligibility Trace (N-Step Q-Learning)
- Annex 2 : CNN 
### 50. Deep Convolutional Q-Learning Intuition
- applied when the environment is an image (vectors/signals)
- The image is sent to the CNN (convolution + pooling)
  - we extract the image features (pixels by pixels) 
  - after flattened we send the results to the Deep Neural Net like before
  - More input signals/states
- Then the Q-Learning algo come to play
  
Ex : Game of Doom

- resources: CNN + Deep Q-Learning

### 51. Eligibility trace

A technic that enables to compute a sets of rewards in advanced and judge them if the cumulative result is good enough
- we keep a **trace** of each reward (negative/positive) in case of a future update 
- the algorithm tracks what action needs to be update
  
Additional resources : 
- Book : "Reinforcement Learning : An Introduction by Richard S. Sutton and Andrew G. Barto (1998)" 
- Chapter 7 : Eligibility trace
  - Temporal differences
  - Monte Carlo Methods
Link : https://mitpress.mit.edu/books/reinforcement-learning

- Book 2: Volodymyr Mnih et al., 2016, Asynchronous Methods for Deep Reinforcement Learning
Link: https://arxiv.org/pdf/1602.01783.pdf

## Section 11: Deep Convolutional Q-Learning Implementation
### 52. Plan of Attack 
Welcome to the Practical Activity of Part 2!

In this part we are going to build and train an AI to play the game of Doom!

1. First, we will build an AI, which will be the Deep Convolutional Q-Learning model combined to Eligibility Trace.

2. Then, we will train it to play the game of Doom.

3. And finally, we will watch a video of our AI playing Doom after it was trained.

The three essential pieces of info you need to know about the environment are the following:

1. The input states are the frames of the game.

2. The possible output actions are: ATTACK, MOVE_RIGHT, MOVE_LEFT, MOVE_FORWARD, MOVE_BACKWARD, TURN_RIGHT and TURN_LEFT. Thus 7 actions in total.

3. The rewards are:
- Plus distance for getting closer to the vest (which is at the end of the corridor).
- Minus distance for getting further from the vest.
- Minus 100 points for getting killed.
### 54. to 69 : Deep Q-Learning Implementation for game of Doom

## Section 12: Deep Convolutional Q-Learning Visualization
### 69 - 73
- see the notebook implementation : 
  - Link : https://colab.research.google.com/drive/1Z8JmCbl-ZMzumYcgyLjWUVNvjtS1ugjz#scrollTo=SXtPVCUGwSfY
## Section 13: - Part 3 - A3C
### 74. Welcome to Part3 - A3C
Welcome to Part 3!

- built an AI that has a brain (Deep Q-Learning) 
- and that can see (Deep Convolutional Q-Learning)
- we will add to it a memory and a critic sense (LSTM-A3C) : 
    - This model is closer to the human brain. 
    - one of the most powerful models in the AI ecosystem. 
- we build an AI to play Breakout


## Section 14: A3C Intuition
### 75. Plan of Attack 
- The 3 A's of A3C
- Actor-Critic
- Asynchronous
- Advantage
- Long Short-Term Memory (LSTM)

### 76. The 3 A's of A3C
A3C - Asynchronous Adavantage Actor-Critic
- Developed by Google DeepMind - 2016

```A3C = Value function + Policy function```

- A3C maintains a policy Pi(at|st;Theta) and an estimate of the value function V (st;Thetav)
- The policy and the value function are updated after every *tmax* actions or when a terminal state is reached

Additional Reading : 
- Asynchronous Methods for Deep Reinforcement Learning by DeepMind - 2016
  - Link : https://arxiv.org/abs/1602.01783
### 77. Actor-Critic
- The output is split into two sets(functions):
  - Actor (Policy function : which action to take or the probability to take an action)
  - Critic (Value function: predicts the value of the state)

### 78. Asynchronous
- several agents attacking the same environment
- the agents have different starting points, therefore they're going to explore the environment in different ways
- they share the experience among each other(they pass knowledge tp each other)
- this methods allow to get the solution faster
- the agents share their experiences through the `Critic-function` which is the same for all of them(allows them to see what's going on in the env)
- From pytorch architecture there is a global NN for all the agents 

Additional reading : 
- Let's make an A3C: Implementation by Jaromir Janish(2017)
  - Link : https://jaromiru.com/2017/02/16/lets-make-an-a3c-theory/
  
### 79. Advantage

`A = Q(s, a) - V(s)`

  - if Q = V  => A ? 
  - if Q > V => A ? 
  - if Q < V => A ? 
  
`A(st, at, Theta, Thetav)` from A3C paper
- Theta : parameter that minimizes the loss function

- tries to minimize the Policy loss based on the Value loss provided by the Critic 
- uses backpropagation to correct the losses


### 80. Long Short-Term Memory (LSTM)
- allows the NN to have a memory of what happen in the previous situation 

- why do we need a memory ? 
  - to store the previous state/action (st-1, at-1)
  - increase output accuracy/prediction (in case of Breakout, guess the preview state of the ball in order to compute the new/present state )

Additional reading : 
- Understanding LSTM Networks : https://colah.github.io/posts/2015-08-Understanding-LSTMs/


## Section 15: A3C Implementation

### 81 to 96
requirements : 
- conda install -c pytorch pytorch - ok
- conda install -c akode gym => 
- conda install -c menpo ffmpeg - ok
- conda install -c conda-forge opencv ?
  - instead : pip install opencv-python 
  
## Section 16: ASC Visualization

### 97 - 98

## Section 17: Annex 1: Artificial Neural Networks
## Section 18: Annex 2: Convolutional Neural Networks
## Section 19: Bonus Lectures

### 124. YOUR SPECIAL BONUS

Hey AI Pro!

Congratulations on completing the Artificial Intelligence A-Z course or even if you completed just part of it! Congrats, it's a great step forward into the World of AI.

What was your favourite part? We really enjoyed watching our AI play Doom! Did you see the expressions on our faces when it killed 5 monsters and got to the end? :)

So now you're probably wondering...

What's next?

Well, there are lots of ways you can go from here.

There are lots of amazing and exciting careers you can build for yourself.

In fact, there are so many paths, that to help you see the big picture we've put together a map for you!

You can find it here: https://sdsclub.com/learning-paths/


It shows in which order to best take our courses.

And if you want our opinion...

Then we truly believe that our Best-Selling Deep Learning A-Z course will be a great supplement to what you learned in the AI course.

You probably have noticed that a large component of the AI algorithms are Artificial Neural Networks.

And even in this course, we have already touched on ANNs and CNNs.

Well, in the Deep Learning course we really take it to the next level and talk even more Neural Networks:

  - Recurrent Neural Networks (RNNs, including LSTMs)
  - Self Organising Maps (SOMs)
  - Boltzmann Machines (RBMs)
  - AutoEncoders (AEs)

This is a comprehensive course on Neural Networks (the most robust one we know of!) and covers both intuition and practical application.

If you haven't checked out our Deep Learning A-Z course yet, then this could be a great next step in your career-building.

Plus, to say thank you for taking our AI course, we'd like to invite you into the Deep Learning A-Z course with a special 90% off coupon:

- https://www.udemy.com/course/deeplearning/?couponCode=YESDATA2022NOV

You are making great progress. Keep ROCKING! 

## Personal Notes

If you want to go even further these courses below might be a big help.

- [What Is an AI Engineer, and How to Become One? - Course article](https://www.coursera.org/articles/ai-engineer)

- [AI For Everyone on](#): 
  - [DeepLearning.AI](https://www.deeplearning.ai/courses/ai-for-everyone/)
  - [Coursera](https://www.coursera.org/learn/ai-for-everyone?trk_ref=articleProductCard)
- [IBM AI Engineering Certificat Professionnel](https://www.coursera.org/professional-certificates/ai-engineer?trk_ref=articleProductCard#courses)



## References 

- [Additional Resource](https://www.tfcertification.com/pages/artificial-intelligence)

- [AI wikipedia](https://en.wikipedia.org/wiki/Artificial_intelligence)

- [DeepMind](https://www.deepmind.com/tags/reinforcement-learning?fc63e648_page=8)

- [Reinforcement learning Implementation with TensorFlow](https://medium.com/emergent-future/simple-reinforcement-learning-with-tensorflow-part-0-q-learning-with-tables-and-neural-networks-d195264329d0)

