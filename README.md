# processing-projects
## COVID-19 Simulator
The COVID-19 Simulator is based on [this Washington Post simulation](https://www.washingtonpost.com/graphics/2020/world/corona-simulator/). In its current state, it simulates a scenario in which people are social distancing. *This is not meant as a real simulation of COVID-19 transmission, nor should it be taken as medical advice.*

The simulator is largely built off of the [CircleCollision](https://processing.org/examples/circlecollision.html) example by Ira Greenberg.

There are two primary classes:`Ball` and `Column`.

**`Ball`** represents a person in the simulation. It is mostly unchanged from the CircleCollision example, but with the addition of a few instance variables that hold the individual's state (e.g. whether or not they are social distancing, their infected/uninfected/recovered state). 

**`Column`** represents a column of the graph that is above the simulation. It calculates the sizes of the rectangles that make up a column based on the ratio between each of the "types" of people (infected, uninfected, recovered). 

Some ways this example might be improved:
* Logic:
  * Make the simulator take deaths into account.
  * Make the distribution of people be less random; maybe base it off of places people would commonly congregate?
  * Make infection probabilistic, people shouldn't _always_ be infected if they come in contact with an infected person
  * Add in a variable for mask usage? Or air conditioning? Or airflow?
* User interface:
  * Allow users to restart the simulator from the interface.
  * Allow users to change parameters within the simulation from the interface.
* Accessibility:
  * Make this visualization usable for colorblind people.
  * Make this visualization usable for people with limited vision (not sure how friendly Processing is screenreaders! I'd be curious to find out.)
