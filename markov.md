# Markov Decision Processes [source](https%3A%2F%2Fbecomesentient.com%2Fmarkove-decision-processes%2F)

- ## Markov Property
  - states that,
  > “The future is independent of the past given the present.”  
  - basically it means that its event that has porbability that is only connected to the present state.
  > Once the current state in known, the history of information encountered so far may be thrown away, and that state is a sufficient statistic that gives us the same characterization of the future as if we have all the history.
  - In mathematical terms, a state St has the Markov property, if and only if;
  > P[S<sub>t+1</sub> | S<sub>t</sub>] = P[S<sub>t+1</sub> | S<sub>1</sub>, ….. , S<sub>t</sub>]
  - transitions can go in matrix like below
    <br><img src="https://becomesentient.com/wp-content/uploads/2021/02/3-1.png"/>

- ## Markov Process
  - Its a squence of states that has the markov property. 
  - Also known as markov chain is a tuple of (S,P) on state space S and transition function P.
    <img src="https://becomesentient.com/wp-content/uploads/2021/02/4-1.png"/> 
  - so you basically have the states and the edges of the graph having weight that represent the probability. 
  - ## Markov Reward Process
    - its a markov process with value judgment, saying how much reward accumulated through some particular sequence that we sampled.
    - An MRP is a tuple (S, P, R, 𝛾) where *S* is a finite state space, *P* is the state transition probability function, *R* is a reward function that says how much immediate reward we expect to get from state *S* at the moment where, <strong><em>R</em></strong><em><sub>s</sub></em> = 𝔼[<strong><em>R</em></strong><em><sub>t+1</sub></em> | <strong><em>S</em></strong><em><sub>t</sub></em> = <em>S</em>], and 𝛾 is discount  factor, where 𝛾 ∈ [0, 1].
    - 𝛾 (discount factor) is basically a value that tells the algorithm how much it should care about rewards now to rewards in the future. If (𝛾 = 0), that means the agent is short-sighted, in other words, it only cares about the first reward. If (𝛾 = 1), that means the agent is far-sighted, i.e. it cares about all future rewards. What we care about is the total rewards that we’re going to get.
    - we use that because for example  imagine you are in a situation, where someone offered you to get a 1000$ now or to get 1000$ after each passing hour for 10 hours, but with each passing hour the value of a 1000$ is decreasing by some factor 𝛾 to the power of the passed hours. As a rational person trying to get the maximum possible amount of money, your choice depends on 𝛾. 
    - If (𝛾 = 0.1), with simple calculation, your return would be,
    - G<sub>t</sub> = 1000 + 100 + 10+ …..,
    - on the other hand, if (𝛾 = 0.9), the return would be,
    - G<sub>t</sub> = 1000 + 900 + 810+ ……
    - Notice that, if the decreasing factor is near zero, you’ll care only about first hour or 2 hours, and stop wasting your time and just leave, i.e. get to the terminal state, all that comes afterward is worthless. If 𝛾 is near 1, you will wait 10 hours to get the money, i.e. still taking actions to get rewards. So 𝛾 defined a horizon for acting in the environment.
    - Sometimes, it’s possible to use undiscounted MRPs (i.e. 𝛾 = 1), if we are sure that all sequences will terminate.
  - ## Markov Decision Process
    - An MDP is a Markov Reward Process with decisions, it’s an environment in which all states are Markov. This is what we want to solve. An MDP is a tuple (S, A, P, R, 𝛾), where S is our state space, A is a finite set of actions, P is the state transition probability function, R is the reward function, and 𝛾 is a discount factor 𝛾 ∈ [0, 1].







