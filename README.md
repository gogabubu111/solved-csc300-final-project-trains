Download Link: https://assignmentchef.com/product/solved-csc300-final-project-trains
<br>
For this assignment, you are to find a solution to a graph problem by utilizing various structures that we have discussed and used this past semester. Your solution should be in C++ and should compile on the class virtual machine. The details for the assignment can be found below. Please take some time to think about and plan out your solution before trying to implement it. This will make things much easier when you try to write the code.

For this project you will be in charge of helping travelers schedule their trips on trains which are leaving and arriving at various stations. You are to create a program that will let a user find a path between two stations among other features. You will be provided with two files:

<ul>

 <li><code>trains.dat</code> which will have the schedule of trains running between stations</li>

 <li><code>stations.dat</code> which contains the list of stations that are in your train network.</li>

</ul>

Your program will provide the following functionality:

<ul>

 <li>Print complete train schedule for all stations</li>

 <li>Print complete train schedule for a specific station</li>

 <li>For a station name, look up station number</li>

 <li>For a station number, look up the satation name</li>

 <li>Determine if there is a direct rout from station A to station B</li>

 <li>Determine if station B can be reached from station A</li>

 <li>For any two stations determine the shortests amount of time it will take to go from A to B wihtout layovers(time should be printed in HH:MM format) If no route exists, alert the user</li>

 <li>For any two stations determine the shortests overall travel time including layovers at stations (time should be printed in HH:MM format) If no route exists, alert the user</li>

 <li>For any two stations determine the shortest overall travel time including layovers at stations when requesting to leave at a certain time (format: HH:MM). In other words a passenger is able to say they want to leave at 09:30 and your program will take this into account when choosing paths</li>

</ul>

Whenever a user is asked for a departure and arrival station they should enter the station numbers. The exception to this is the look up station id by name function

<h2><a id="user-content-input-files" class="anchor" href="https://github.com/Ballcapz/Trains#input-files" aria-hidden="true"></a>Input Files</h2>

Your program will read in 2 input files

<ul>

 <li><code>stations.dat</code></li>

 <li><code>trains.dat</code></li>

</ul>

<h3><a id="user-content-stationsdat" class="anchor" href="https://github.com/Ballcapz/Trains#stationsdat" aria-hidden="true"></a>stations.dat</h3>

<code>stations.dat</code> contains the mapping of station names to their unique id numbers. The file format will consist of a series of ID and name pairs. An example would look similiar to

<pre><code>1 madison2 brookings3 sioux_falls4 fargo</code></pre>

You can assume the following about <code>stations.dat</code>

<ul>

 <li>The station id’s will fall in the range of 1 to 199</li>

 <li>The id’s may not be sequencially in order</li>

 <li>Each station name will be at most 25 characters in length and no spaces will be included</li>

 <li>The file will not specify how many stations are in the file</li>

</ul>

<h3><a id="user-content-trainsdat" class="anchor" href="https://github.com/Ballcapz/Trains#trainsdat" aria-hidden="true"></a>trains.dat</h3>

This file contains information regarding the trains that will be traveling between the various stations. The information contained in this file includes the departure and arrival station id’s as well as the departure and arrival times in 24 hour time. A sample file would look similiar to

<pre><code>1 2 0830 11201 4 1100 15403 2 1200 16004 3 1600 18002 1 0900 1000</code></pre>

You can assume the following about the trains.dat file

<ul>

 <li>The arrival and departure times will always be 4 digits in length</li>

 <li>No trains will cross the midnight mark. In other words no train would leave the stations at 2300 and arrive at 0130 the next morning</li>

 <li>The arrival and departure times will be in 24 hour time with no colon seperating the hours from minutes</li>

</ul>

<h2><a id="user-content-expectations" class="anchor" href="https://github.com/Ballcapz/Trains#expectations" aria-hidden="true"></a>Expectations</h2>

This assignment is much more free form then the ones i have given you previously. There is no expected output file to match or provided header file implementations to meet. You should take this as an opportunity to show what you have learned over the past semester to implement a more ambitious program(even an extremely arbitrary one). Choose your structures wisely and this is actually fairly strait forward. The STL library or other built in libraries for stacks/queues/vectors are open for use with the exception of any prebuilt graphing structures or algorithms

<h2><a id="user-content-example-output" class="anchor" href="https://github.com/Ballcapz/Trains#example-output" aria-hidden="true"></a>Example Output</h2>

<pre><code>======================================================================== READING RAILWAYS SCHEDULER========================================================================Options - (Enter the number of your selected option)(1) - Print full schedule(2) - Print station schedule(3) - Look up stationd id(4) - Look up station name(5) - Servie available(6) - Nonstop service available(7) - Find route (Shortest riding time)(8) - Find route (Shortest overall travel time)(9) - ExitEnter option: 2Enter station id: 1Schedule for madisonDeparture to brookings at 0830, arriving at 1120Departure to fargo at 1100, arriving at 1540Arrival from brookings at 2200Enter option: 4Enter station name: madisonmadison's station id is 1Enter option: 5Enter departure station id: 1Enter destination station id: 2Service is available from madison to brookingsEnter option: 7Enter departure station id: 2Enter destination station id: 3Time on train to go from brookings to sioux_falls is 7 hours and 40 minutesItinerary---------Leave from brookings at 0900, arrive at madison at 1000Leave from madison at 1100, arrive at fargo at 1540Leave from fargo at 1600, arrive at sioux_falls at 1800Enter option: 9Goodbye!</code></pre>