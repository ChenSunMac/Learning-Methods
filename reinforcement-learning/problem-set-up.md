# Problem Set Up

The basic component of a RL set up will be _Actor_ \(player/model\), _Environment_ \(game/real environment/other agent\), _reward function_ \(pseudo rule/score\).

To formalize a RL problem, we can use Markove Decision Process, defined by: $$(\mathcal{S}, \mathcal{A}, \mathcal{R}, \mathbb{P}, \gamma)$$, where

* $$\mathcal{S}$$ : set of possible states
* $$\mathcal{A}$$ : set of possible actions
* $$\mathcal{R}$$ : distribution of reward given \(state, action\) pair
* $$\gamma$$ : discount factor

![](../.gitbook/assets/screenshot-from-2019-07-17-17-35-05.png)

## How good is a state?

**Value Function** at state s, is the expected cumulative reward from following the policy from state s:

$$
V^{\pi}(s)=\mathbb{E}\left[\sum_{t \geq 0} \gamma^{t} r_{t} | s_{0}=s \right]
$$

## How good is a state-action pair?

**Q-value function** at state s and action a, is the expected cumulative reward from taking action a in state s and then following the policy:

$$
Q^{\pi}(s, a)=\mathbb{E}\left[\sum_{t \geq 0} \gamma^{t} r_{t} | s_{0}=s, a_{0}=a \right]
$$

