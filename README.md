# DJS05 Project Brief: Building a Redux-Inspired Store for a Tally App

This project implements a simple tally counter using a state management approach inspired by Redux. The core concept revolves around managing a single piece of state — the tally value — which starts at 0. The application can modify this state using three key actions: `ADD`, `SUBTRACT`, and `RESET`. The `ADD` action increases the tally value by 1, `SUBTRACT` decreases it by 1, and `RESET` sets the tally value back to 0. 

To handle state management, I created a custom store that encapsulates the state and provides methods to interact with it. These methods allow actions to be dispatched, the current state to be accessed, and subscribers to be notified of any changes to the state. Every time the state changes due to an action, the new state is logged to the console for easy tracking and debugging.

The primary challenge I encountered during development was ensuring that each action was correctly reflected in the state. To solve this, I implemented a simple reducer function. The reducer takes the current state and an action as inputs, and based on the action type, it returns a new state. This ensures that the state transitions happen in a predictable and controlled manner.

For the purpose of testing and running this code, I included an `index.html` file. By opening this file in a browser, you can see the tally counter in action, with each state change being logged in the browser console for visibility.

While this implementation is functional, it could certainly be improved in terms of modularity, maintainability, and scalability. For example, if the project were to grow, it would make sense to split the code into separate JavaScript files for better organization. These files might include `store.js` to manage the store, `reducer.js` for the state-changing logic, `actions.js` to define the action creators, and `main.js` to orchestrate the application logic. However, since this project is quite small and straightforward, I chose to keep everything in one file for simplicity and quick iteration.

In retrospect, if I were to expand on this project, I would definitely adopt a more modular structure, which would make it easier to add new features or modify existing functionality without breaking the codebase. Additionally, incorporating more advanced concepts such as middleware or asynchronous actions could further enhance the capabilities of the state management system, making it more adaptable for larger, more complex applications.












.

In this challenge, you will venture into the realm of state management by constructing a Redux-inspired store to manage the state of a simple Tally App. Your primary goal is to manage the app's state changes efficiently, focusing on core functionalities like incrementing, decrementing, and resetting a counter. Instead of rendering changes on the UI, you'll subscribe to state updates and log them to the console, highlighting the power of state management in applications.

## Objective
Create a minimalistic, Redux-inspired store to manage and log the state of a counting Tally App. Your implementation will not involve UI rendering; instead, it will use console logs to demonstrate state management effectively.

Observer Pattern resource from Refactoring Guru: https://refactoring.guru/design-patterns/observer

## User Stories (Gherkin Syntax)
Your challenge will encompass the following scenarios, tested through your store's implementation:

### SCENARIO 1: Initial State Verification
```
GIVEN no interactions have been performed yet
WHEN the “getState” method is run
AND the result is logged to the console
AND the browser console is open
THEN the state should show a count of 0
```

### SCENARIO 2: Incrementing the Counter
```
GIVEN no interactions have been performed yet
WHEN an “ADD” action is dispatched
AND another “ADD” action is dispatched
AND the browser console is open
THEN the state should show a count of 2
```

### SCENARIO 3: Decrementing the Counter
```
GIVEN the current count in the state is 2
WHEN a “SUBTRACT” action is dispatched
AND the browser console is open
THEN the state should display a count of 1
```

### SCENARIO 4: Resetting the Counter
```
GIVEN the current count in the state is 1
WHEN a “RESET” action is dispatched
AND the browser console is open
THEN the state should display a count of 0
```

## Requirements
- **Implement a Global Store**: Create a Redux-inspired store that holds the state of the tally counter. The store should have the ability to dispatch actions and subscribe to state changes.
- **State Management Functions**:
  - **getState**: Returns the current state.
  - **dispatch**: Takes an action (e.g., ADD, SUBTRACT, RESET) and updates the state accordingly.
  - **subscribe**: Accepts a function that gets called whenever the state changes. This function should log the new state to the console.
- **No UI Rendering**: This challenge focuses on state management without the complexity of UI rendering. All state changes should be observable through console logs.
- **Functional Programming Principles**: Draw upon functional programming concepts as illustrated in the reference videos. While Redux is the inspiration, you're encouraged to apply these principles creatively in your implementation.

## Submission Guidelines
Your submission should consist of a JavaScript file(s) that encapsulate your Redux-inspired store and the logic for dispatching actions and subscribing to changes. Include a README.md file explaining:
- How to run your code.
- A brief overview of your approach.
- Any challenges you faced and how you overcame them.

Ensure your code is well-commented and adheres to best practices for readability and maintainability.

## Evaluation Criteria
- **Correctness**: Your implementation should correctly handle the scenarios as outlined in the user stories.
- **Code Quality**: Use of functional programming principles, clear naming conventions, and code organization.
- **Documentation**: Clarity of your approach and reflections in the README.md.

This challenge is an excellent opportunity to demonstrate your understanding of state management concepts and functional programming principles. Good luck!
