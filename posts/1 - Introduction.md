Introduction

Hello everyone. Welcome to the series during which we are going to design and implement a real-world example of an event-driven system.
We find the lack of such examples as one of the largest obstacles to larger adoption of event-driven systems.
With this series we hope to get the attention of the community, involve people in the discussion and build a comprehensive example that would represent a useful resource on learning how to build robust, performant and stable event-driven systems in the real-world.

When it comes to the business domain, we have chosen to use cinema ticket sales as our example.
It was chosen because it offers a significant amount of complexity to justify the use of an event-driven design approach and is fairly easy to understand.
However, in order to reduce the complexity and size of the initial solution, we chose to introduce some restrictions:

- All reservations and ticket sales are done online (no counters),
- No support for refunds through software,
- Projection duration includes duration of a movie, commercials and cleanup time before another projection,
- All sets cost the same.

We plan to remove these restrictions after the initial implementation and also implement some additional features that we found useful but not required for the initial implementation during our planning.
This way we will show how your system can evolve and how event sourcing enables us to perform design changes without complex migrations.

The concrete implementation approach is not yet completely defined but we do have some general guidelines we would like to follow.
We are going to use the event modeling to design the system and event sourcing for the technical implementation.
We found that Event Modelling is ideal for maintaining conceptual integrity when it comes to the development of information systems.
It uses specification by example and four design patterns.
With Event Modelling a person can get the feeling of how the system behaves (emitting events) depending on the given inputs (commands) by looking at one simple picture.
This makes it easy for beginners or new team members to join the ongoing project.
We found that Event Sourcing is a well fitted approach for implementing event-driven systems.
Development will kick off with .NET and ReactJS.
Using events for communication will allow us to implement different components with different technologies later.
We’ll start with a monolithic system structure which will be modular so we can split it into multiple independent components later.
That way we’ll show how the system can evolve in terms of the architecture over time.
All the code will be available through the public repository.
People are encouraged to fork, create issues and pull requests against that repository.
We hope for the community to engage and help us in steering the development of this example along the way or spread the word by sharing the content with the others.
Creating the solution with another tech stack, different implementation approach and features is also much appreciated and welcomed.

We hope you will join us on this path of discovery and learning.
Next blog post in this series will focus on how we did the initial design of the system using event modeling techniques.

Until next time,
@culaja, @rmilovic90, @the_milenkara .
