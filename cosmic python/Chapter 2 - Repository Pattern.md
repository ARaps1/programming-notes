
- It is an abstraction layer that allows to separate our model layer with our data layer.
- The Repository pattern is a simple abstraction around permanent storage
- Our domain model should be free of infrastructure concerns, so your ORM should import your model, and not the other way around.


### Questions:
- What are some pros/cons you see with the Repository pattern? 
- Do you guys see any limitations with our implementation of Repository pattern at Benchling?
- Can you think of scenarios where the Repository pattern might introduce more complexity than it solves? What are the warning signs that this pattern might be overkill?
- Where do you draw the line between just implementing your backend doing simple CRUD over to using Domain driven design? Or would you always set out to build with the layers in mind?
- The Repository pattern aims to simplify the interaction with the database, but do you think there’s a point where it might actually add unnecessary complexity? How would you recognize that in a project?