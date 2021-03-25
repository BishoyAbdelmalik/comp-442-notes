# Markov Decision Processes [source](https%3A%2F%2Fbecomesentient.com%2Fmarkove-decision-processes%2F)

- ## Markov Property
  - states that,
  > “The future is independent of the past given the present.”  
  - basically it means that its event that has porbability that is only connected to the present state.
  > Once the current state in known, the history of information encountered so far may be thrown away, and that state is a sufficient statistic that gives us the same characterization of the future as if we have all the history.
  - In mathematical terms, a state St has the Markov property, if and only if;
  > P[S<sub>t+1</sub> | S<sub>t</sub>] = P[S<sub>t+1</sub> | S<sub>1</sub>, ….. , S<sub>t</sub>]
  - transitions can go in matrix like below
    <img src="https://becomesentient.com/wp-content/uploads/2021/02/3-1.png"/>

- ## Markov Process
  - Its a squence of states that has the markov property. 
  - Also known as markov chain is a tuple of (S,P) on state space S and transition function P.
    <img src="https://becomesentient.com/wp-content/uploads/2021/02/4-1.png"/> 
  - so you basically have the states and the edges of the graph having weight that represent the probability. 
  - ## Markov Reward Process
    - its a markov process with value judgment, saying how much reward accumulated through some particular sequence that we sampled.
    - An MRP is a tuple (S, P, R, 𝛾) where *S* is a finite state space, *P* is the state transition probability function, *R* is a reward function where, <strong><em>R</em></strong><em><sub>s</sub></em> = 𝔼[<strong><em>R</em></strong><em><sub>t+1</sub></em> | <strong><em>S</em></strong><em><sub>t</sub></em> = <em>S</em>],
    - 


