#### **Quality Functions**

- $Q(s,a)$: Represents the **quality of a state-action pair**, indicating how good it is to take action $a$ in state $s$.
- **Value Function**: Measures the expected return from a state $s$, denoted as $V(s)$.
- **Policy ($\pi$)**: A strategy defining the action $a$ to take in state $s$, expressed as $\pi(s) = a$.

---

#### **Value Iteration**

- Value iteration involves choosing actions to **maximize** the value function $V(s)$, ensuring the best possible action is taken.
- Actions are selected to satisfy:  
    $V(s) = \max_a \sum_{s'} P(s'|s, a) \left[ R(s, a, s') + \gamma V(s') \right]$

---

#### **Bellman's Equation**

- **State Value Function**:  
    $V(s) = \max_a \sum_{s'} P(s'|s, a) \left[ R(s, a, s') + \gamma V(s') \right]$
- **Q-Value Function**:  
    $Q(s,a) = \sum_{s'} P(s'|s, a) \left[ R(s, a, s') + \gamma \max_{a'} Q(s', a') \right]$

---

#### **Markov Decision Process (MDP)**

- A mathematical framework for modeling sequential decision-making under uncertainty.
- Consists of:
    - **States** ($S$): Possible situations.
    - **Actions** ($A$): Choices available to the agent.
    - **Transition Probabilities** ($P(s'|s, a)$): Probability of reaching $s'$ from $s$ by taking $a$.
    - **Reward Function** ($R(s,a,s')$): Immediate reward after transitioning.
    - **Discount Factor** ($\gamma$): Future reward significance.

---

#### **Monte Carlo Learning**

- **Model-Free** approach: Relies purely on **trial and error** without prior knowledge of the environment.
- **Episodic Learning**: Learning occurs after episodes (definitive end).
- Update rule for value function:  
    $V(s) \leftarrow V(s) + \alpha \left[ G_t - V(s) \right]$  
    where:
    - $G_t$: Return from time $t$.
    - $\alpha$: Learning rate.

---

#### **Q-Learning Update Equation**

- Monte Carlo Q-learning update rule:  
    $Q_{\text{new}}(s, a) = Q(s, a) + \alpha \left[ R + \gamma \max_{a'} Q(s', a') - Q(s, a) \right]$  
    where:
    - $Q(s,a)$: Current Q-value.
    - $R$: Reward for action $a$ in state $s$.
    - $\gamma$: Discount factor.
    - $\max_{a'} Q(s', a')$: Maximum Q-value for the next state $s'$.

