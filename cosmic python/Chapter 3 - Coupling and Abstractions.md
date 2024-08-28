- Coupling:
	- When components are too intertwined at a point where they cannot be independently modified without affecting the other
	- it increases the risk and cost of changing our code
	- This is beneficial if our components have high cohesion but a pain if not
	- We can reduce the dependencies between two systems if they have an abstraction layer in between to interact with
- Edge to Edge testing:
	- is a type of testing that focuses on the interactions between different components or systems



Questions:
- What makes a good abstraction? 

- How do you approach refactoring legacy code that is tightly coupled? What steps do you take to ensure you are not breaking any existing functionality?

- How do you determine the right level of abstractions in your own projects?

- In Chapter 3, the author points out his strategy to refactoring the transferring file from one directory to the other. The steps were to:
	  - determine the different tasks that needs to be done
	  - giving each task to a clearly defined actor
	Are there any strategies you guys suggest for introducing abstractions and reducing coupling?

- What is Edge to Edge testing?

- An interesting take the book had, was that mocking modules in test are code smell? I see us doing mocks at Benchling at the time, any takes on why that has not changed?

- Would you guys agree that here at Benchling our unit tests have become "Integration tests"?