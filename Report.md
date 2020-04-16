# DeepRL-Navigation
Project 1 "Navigation" of the Deep Reinforcement Learning nanodegree.

## Learning Algorithm

To be honest, I copied and pasted the source code of the Jupyter notebook "Deep_Q_Network_Solution.ipynb" of Part 2. Value-Based Methods; Lesson 2: Deep Q-Networks; 7. Workspace. Because Udacity allows us to do it in Part 2: Value-Based Methods; Project: Navigation; 7. Not sure where to start?

<p align="center">
 <img src="/images/not-sure-where-to-start.png" width="50%">
</p>

I copied the solution code because I'm sick of Covid-19. Fortunately, I'm recovering. I feel very tired. Otherwise I'm an expert in Deep Reinforcement Learning as you can see in the seminars I gave last year:

Webinar on Deep Reinforcement Learning (Secure & Private AI Scholarship Challenge)<br/>
https://youtu.be/oauLZG9nAX0

Deep Reinforcement Learning (IEEE Computer Society)<br/>
https://youtu.be/rf91xKkoP6w

In summary, Deep Reinforcement Learning (Deep RL) is an extension of Reinforcement Learning (RL) that uses Deep Learning techniques in order to handle complex continuous states instead of simple discrete states. RL is the branch of artificial intelligence that programs algorithms capable of learning and improving from experience in the form of SARS tuples: State 0, Action, Reward, and State 1. This kind of algorithms and problems are very general because they are based on search algorithms, general problem solvers (GPS), and statistics.

The solution code I copied uses:
- Vanilla Deep Q-Network;
- Double Deep Q-Network to avoid oscillations caused by overestimated rewards;
- Experience Replay in order to keep training the Q-Network with past experiences;
- Epsilon Greedy with geometric decay of 0.995, in order to balance exploration at the begining (epsilon=1) versus explotation at the end (epsilon=0.01);
- Adam optimizer with learning rate of 5e-4;
- BATCH_SIZE=64 (the number of experience tuples per training iteration);
- GAMMA=0.99 (the Q-Network is aware of the intermediate future, but not the far future);
- A deep neural network to represent complex continuous states.

The deep neural network to represent complex continuous states has:
- A linear fully-connected layer of dimensions state_size=37 and fc1_units=64;
- A linear fully-connected layer of dimensions fc1_units=64 and fc2_units=64;
- A linear fully-connected layer of dimensions fc2_units=64 and action_size=4.

## Plot of Rewards

The Q-Nework was trained for 706 episodes. In each episode, the agent is trained from the begining to the end of the simulation. Some episodes are larger and some episodes are shorter, depending when the ending condition of each episode appears. Each episode has many iterations. In each iteration, the Q-Network is trained with `BATCH_SIzE=64` experience tuples (SARS).



```
Episode 100	Average Score: 0.96
Episode 200	Average Score: 4.39
Episode 300	Average Score: 7.77
Episode 400	Average Score: 10.41
Episode 500	Average Score: 12.49
Episode 600	Average Score: 14.25
Episode 700	Average Score: 14.91
Episode 706	Average Score: 15.07
Environment solved in 606 episodes!	Average Score: 15.07
```

![Plot of rewards (training)](/images/plot-of-rewards-training.png)

![Plot of rewards (testing)](/images/plot-of-rewards-testing.png)

## Ideas for Future Work
