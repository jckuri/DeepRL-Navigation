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
- Epsilon Greedy in order to balance exploration at the begining versus explotation at the end;
- A deep neural network to represent complex continuous states.

## Plot of Rewards

![Plot of rewards (training)](/images/plot-of-rewards-training.png)

![Plot of rewards (testing)](/images/plot-of-rewards-testing.png)

## Ideas for Future Work
