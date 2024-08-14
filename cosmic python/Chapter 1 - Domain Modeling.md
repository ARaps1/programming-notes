
### Encapsulation and Abstraction
- simplifying behavior and hiding the data
- When we encapsulate code, we provide a task or action for it to perform and hiding under a well defined function or class
- Encapsulating behavior leads to having easier to read and organized code. We keep high level of abstractions and hide implementation details under well defined objects and functions


### Layering
- we layer code to reduce dependencies between files and classes.
- Common three layers:
	- Presentation Layer
	- Business Layer
	- Database Layer
### The Dependency Inversion Principle
- High level modules should not depend on low-level modules. Both should depend on abstractions
	- high level = code that your org really cares about (related to domain, like users, entries,)
	- low level = code that it doesn't care about like network sockets, filesystems
- Abstractions should not depend on details. Instead the details should be based on the abstractions.
- Adding abstractions between them allows the two change independently from each other



### Domain Modeling
- it is the problem you are trying to solve and represents the business logic.
- is the mental map that business owners have of their business 


### Business Knowledge
- The project is modeling the interactions of an e-commerce platform and its warehouse and shipments
- Buying team buys products in batches.
	- reference
	- sku
	- quantity
	- eta
- You can allocate order lines to batches and an order line is represented by:
	- reference
	- sku
	- quantity
- Restrictions:
	- you cannot allocate the same order line twice to a batch
	- you cannot allocate an order line to a batch if the batch contains less quantity available than the order's quantity
	- allocations should prefer in stock batches over batches in shipment and prioritize batches over ETA
	- 
### Property
- use this decorator when you want to protect an attribute behind setter, getter, deleter without having to implement them

#### Value Object Pattern
- Use the value object pattern whenever we have a business concept that has data but no identity.
- A value object is any domain object that is uniquely identified by the data it holds. Mostly immutable
- Any object that is identified only by its data and doesn't have a long lived identity. You change its value and it represents something else
#### Entity
- Entities, unlike values, have identity equality. A long lived identity. You can change its values and still recognizably the same thing

### Recap:
- Domain Modeling: part of the code that is closest to business. Mind map of business or the problem you are solving
- Distinguish entities from value objects:
	- value objects are immutable and are represented by its attributes. If you change them, it represents a total different object identity.
	- entities are object that has attributes and is mutable. Changing its attributes does not change its identity. E.g, Person, Car, Building, Account
		- Entities must have a unique identifier
- Use functions too, it doesn't have to be an object

### Questions
- I feel a bit confused between value objects and entities, it seems sometimes kind of hard to know whether an object has a long lived identity or not. For example, the Value Object can still be defined by class and have an id. It can still be changed as well like changing the quantity of an order. In the case of it being immutable makes sense, but if it is mutable what would be difference between value object pattern and entities?





