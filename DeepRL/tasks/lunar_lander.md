### Assignment: lunar_lander
#### Date: Deadline: Nov 11, 23:59
#### Points: **compulsory** & **7 bonus**

Solve the [LunarLander-v2 environment](https://gym.openai.com/envs/LunarLander-v2)
environment from the [OpenAI Gym](https://gym.openai.com/). Note that this task
does not require TensorFlow.

Use the supplied [lunar_lander_evaluator.py](https://github.com/ufal/npfl122/tree/master/labs/03/lunar_lander_evaluator.py)
module (depending on [gym_evaluator.py](https://github.com/ufal/npfl122/tree/master/labs/02/gym_evaluator.py)
to interact with the discretized environment. The environment
methods and properties are described in the `monte_carlo` assignment,
but include one additional method:
- `expert_trajectory() → initial_state, trajectory` This method generates
  one expert trajectory and returns a pair of `initial_state` and `trajectory`,
  where `trajectory` is a list of the tripples _(action, reward, next_state)_.
  You can use this method only during training, **not during evaluation**.

To pass the task, you need to reach an average return of 0 during 100 evaluation episodes.
During evaluation in ReCodEx, three different random seeds will be employed, and
you need to reach the required return on all of them. Time limit for each test
is 5 minutes.

The task is additionally a _competition_ and at most 7 points will be awarded
according to relative ordering of your solution performances.

You can start with the [lunar_lander.py](https://github.com/ufal/npfl122/tree/master/labs/03/lunar_lander.py)
template, which parses several useful parameters, creates the environment
and illustrates the overall usage.
