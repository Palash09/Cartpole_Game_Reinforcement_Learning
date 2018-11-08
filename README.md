# Reinforcement_Learning

Here reinforcement learning is implemented using OpenAI Gym library with one of the environment i.e. CartPole. So let's understand the code
and look at how we can implement Reinforcement Learning.

Step 1: 
First we are importing the gym library which we had installed earlier. 
Then we are using one of the inbuilt environments of Gym i.e. CartPole. 
This environment will display a pole trying to balance on a cart which is moving left and right.

Step 2:
Here we have created a function which will take care of the action which should be taken by the agent on the basis of state and environment. 
Using this function, our main aim is to maintain the pole present on the cart should try to balance and not fall down. 
So if the pole bends more than a given angle we are returning 0 as a result.

Step 3:
In this total list, we are storing rewards which will be collected 

Step 4:
Here in this loop we are calculating the rewards obtained in each episode by going over the loop. 
Each loop starts with an observation value which has been reset using reset () function.

Step 5:
Here we are running an instance of CartPole environment for 1000 timesteps, which will fetch the environment each time. 
There will be a small popup window displaying cart-pole using the render () function. Along with this, 
we are deciding the current action based upon the observation obtained by the agent’s previous actions by calling the basic_policy() function.
Now next we have used step () function which will return four values which are observation: object type (this will tell about the observation 
of the environment), reward: float type (amount of reward received by previous action), done: Boolean type (this tells about whether the 
episode has terminated or not), and info: dictionary type (the information provided by this dictionary is used for debugging and also for 
learning about the environments). So in this loop, at each timestep the agent chooses an action and the environment returns an observation 
and a reward. Lastly in the loop once the done variable returns the value as “true”, then we come out of the loop and append the 
episode_rewards value to the totals[].

Step 6:
Finally we are printing the totals [] list which has the maximum rewards values and along with this, 
we are printing the maximum reward obtained. 
Most importantly we are using close () function to close the pop-up window otherwise, the program may crash.

