Download link for project- https://drive.google.com/file/d/15GWYQYBbwLgAk81eI_j-JS_5ZKlKQbDh/view?usp=sharing
(File size was too large for GIT)
GOAP AI system demonstration. 

The GOAP system was set up with virtual GOAPActor and GOAPAction classes alongside a 
GOAPPlanner, which handled all the available actions and analyzed the current World State of 
the level to build a valid sequence of Actions for the GOAPActors. Regarding the GOAP actors in 
the level, they were given actions with preconditions of whether or not they had the resources 
that were coded as Goal States and avoiding hunger by eating food whenever their HP was low 
enough. Here the Actors would not begin an action unless they were not hungry, that being a 
precondition added to the actions related to picking up and dropping off resources. If not 
hungry, the actors engage in 2 actions that allow them to carry resources to the appropriate 
static actors on the map, this being the Pickup and Dropoff actions. In each action the actors 
would decrement the resources from the Resource actors and increment their own resources 
class variables after reaching a distance within a threshold of the relevant Pick up and Drop off 
points. 

In particular for the Builder Actor, I decided to make the Builder wait for sufficient 
enough resources at the Village center before leaving to the building site in order to maintain 
the efficiency of the process of taking the resources and then building at the Building site. 
I decided to make the move speed of the actors relatively fast to making testing easier and to 
ensure resources could be taken quickly enough so that actors would be able to finish a set of 
actions without running low on HP. I decided to use the sphere collision-based system as shown 
in the labs that checked if each predetermined actor was close enough to the main GOAPActor 
doing the action. I felt it was appropriate and effective for the implementation required. It 
allowed accurate tracking of all the necessary actors even if it was not quite as efficient as 
possible. 


Each GOAPActor had their own specific action class to be able to give more properties to each 
action. Through use of polymorphism the GOAPActors are also able to have their own unique 
class variables within the system, this is used in particular to keep track of the resources each 
Actor has at any given time and for each actor to have their own specific resources that they 
are able to carry.
