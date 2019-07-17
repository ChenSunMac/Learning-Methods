# Problem Set Up

The basic component of a RL set up will be *Actor* (player/model), *Environment* (game/real environment/other agent), *reward function* (pseudo rule/score).

To formalize a RL problem, we can use Markove Decision Process, defined by: $$(\mathcal{S}, \mathcal{A}, \mathcal{R}, \mathbb{P}, \gamma)$$, where 
- $$\mathcal{S}$$ : set of possible states
- $$\mathcal{A}$$ : set of possible actions
- $$\mathcal{R}$$ : distribution of reward given (state, action) pair
- $$\gamma$$ : discount factor


### How good is a state? 

**Value Function** at state s, is the expected cumulative reward from following the policy from state s:

$$
V^{\pi}(s)=\mathbb{E}\left[\sum_{t \geq 0} \gamma^{t} r_{t} | s_{0}=s \right]
$$

### How good is a state-action pair?

**Q-value function** at state s and action a, is the expected cumulative reward from taking action a in state s and then following the policy:

$$
Q^{\pi}(s, a)=\mathbb{E}\left[\sum_{t \geq 0} \gamma^{t} r_{t} | s_{0}=s, a_{0}=a \right]
$$
