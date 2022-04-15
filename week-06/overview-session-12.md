# Session-12

Tonight we reviewed **Iteration Methods** and learned about **State Machines**

We started class off by:

- **Adding functionality to our CakeFactory lab** by creating and implementing an `eat()` function.

- **Coding _a solution_ for the Titleize lab** using some super helpful methods including:

  - `.map()`
  - `.join()`
  - `.split()`

- **Discussing the reduce method**
  [MDN: Reduce Method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)

We spent the rest of class learning about...

## State Machines

A State Machine:

- Is a system with a limited number of defined 'states';
- Can only be in one 'state' at a time;
- Has well defined rules to 'transition' between states.

A helpful analogy is a **Traffic Light**. There are three _states_ for a traffic light (green, yellow, red).

Similar to a state machine, a traffic light can only be in one state at a time (e.g. can't be green AND red at the same time.) There are also rules that determine its functionality.

**Why use a State Machine??**

- _Clarity_
- _Predictability_
- _Fail-fast debugging_ -- Many bugs are due to the system receiving unexpected input, or input that is inappropriate at the moment

**What is State??**

_The term "state" has several overlapping meanings:_

- In general, "state" means any data
  - especially in Object Oriented Programming, e.g. "state and behavior" means "instance variables and instance methods"
- In particular, "state" means "there is a clear state transition diagram at work here"

**Implementing a State Machine**

Here is an example of how to implement a state machine:

```js
let states = {
  green: { canChangeTo: ["yellow"] },
  yellow: { canChangeTo: ["red"] },
  red: { canChangeTo: ["green"] },
};

let currentState = "green"; // create an initial state

function enterState(newState) {
  let validTransitions = states[currentState].canChangeTo;
  if (validTransitions.includes(newState)) {
    currentState = newState;
  } else {
    throw (
      "Invalid state transition attempted - from " +
      currentState +
      " to " +
      newState
    );
  }
}
```

## Reading & Homework

- [Walkway-objects](https://replit.com/@Upright-JSI-Mar-2022/walkway-objects#index.js)
- [Tag-Search](https://replit.com/@Upright-JSI-Mar-2022/tag-search#index.js)
- [Fibonacci-Stack](https://replit.com/@Upright-JSI-Mar-2022/fibonacci-stack#index.js)
- [Traffic-Light](https://replit.com/@Upright-JSI-Mar-2022/traffic-light#index.js)


