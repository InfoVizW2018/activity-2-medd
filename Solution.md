
SEASPAN FERRY SCHEDULE VISUALIZATION
===================================

## INTRODUCTION

SEASPAN Ferries needs an efficient visualization table which could enable them to understand the following:
  * What Each Vessel is doing at any given time, it's occupancy (Vehicle and Passenger) and direction it's travelling.
  * The availablity of berths in the ports.
  
The below are the Constraints that we need to understand while making changes to the schedule:
 * A ship has travel time, cannot teleport, cannot carry more passengers than its capacity.
 * A ship cannot dock when no berths are available in the ports.
 
We have the below Assumptions:
 * We assume ships occupancy is divided into Vehicle and Passengers.
 * We assume only Tilbury has 3 berths and others have 2 berths available for SEASPAN ferries.
  
  
## Solution

We present an interactive tool (shown bellow) which shows the positions of vessels, their direction of travel, occupany, time of travel, destination, origin along with the status of the ports (berths). Here we represent ports as rectangles. The smaller red rectangles attached to the port rectangle shows the number of berths. If a berth is occupied by the ship, the id of the occupied ship would be written inside the rectangle. The course between the ports are marked by unique colors on the interactive screen.
![Image](https://github.com/InfoVizW2018/activity-2-medd/blob/master/visual.jpg)
The ships are represented as Rectangles with a small triangle in front which indicates the direction of travel. The vessels are also marked by the vessel id. The rectangle shape of the vessel is further divided into 2 sub rectangles each for passenger occupany and vehicle occupancy. Occupancy is written with % occupied and using legends- Green for passengers and blue for vehicles. The legends are marked in the screen itself.

Clicking on the ship would highlight its source and destination ports. The time of departure will be popped up and shown at the departure port and time of arrival at the arrival port. The machine learning model would also indicate the predicted occupancy considering the time and day of the week. This information could help me officers adjust schedules accordingly.

The time and day are adjusted using the sliders and calenders as required (At bottom of the map). We also provide and edit schedule as required. Once a schedule is added/changed, an automatic simulation would be done to study its feasiblity. This would take into account, the machine learning predictions. average route time, average availablity of the berths in the ports, passenger and vehicular occupancy etc. The system would highlight the bottle necks (Like ships anchored outside ports waiting for berths)
 
## What, How and Why ?

What - A multi dimensional table.
Why
 * Analyze: Consume (Using the table) and Produce (when we change/edit schedule and simulate)
 * Search:  LookUp (particular vessel/port at a particular time) and Browse (When we use the slider going through schedule)
 * Query : Summarize
 
How
 * Map- Shapes, Colors and Motion (Interactive Map)
 * Manipulate - We are doing change, navigate and select.
 


## Design Study Methods

**Pre-Condition Phase**
* Learn: Analyze all the avaiable Machine learning, Simulation and Visualization tools which are popular.
* Minnow: Our colloborators would be schedule officers from SEASPAN, Simulation experts from industry and data would be from reservation and travel history database of SeaSpan, Time frame: Would be an year if data collection is required.
* Cast: We developers are the front end analyst and SEASPAN officials would be gatekeepers.

**Core Phase**

* Discover: Anomolies in data due to season and climate changes.
* Design: Design of the tools from various options such as tools, machine learning frameworks and statistical techniques.
* Implement: Rapid Prototyping and MVP
* Deploy: Show the working tool/ Prototype to the SEASPAN officials and get feedback

**Analysis Phase**

* Reflect: Can this tool be used for other bus/train/ship/ferry services across the world.
* Write: Write a design study paper on our experience in designing schedule visualization tool for transport services

## Pitfalls

* PF-2 premature start: insufficient knowledge of vis literature.
* PF-4 no real data available (yet).
* PF-11 no rapport with collaborators.
* PF-12 not identifying front line analyst and gatekeeper before start.




