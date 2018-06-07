Readme:

---- ValetParking Assistant ----
HOW TO USE:

ValetParkingAsssistant is a project folder. It can be imported into Eclipse.

This site will allow you to access the programing environment to open my folder.
http://developer.android.com/sdk/index.html

After you download the ADT. You need to open up eclipse and import the project in the file menu.

Instructions on running the application using a virtual machine or Android device can be seen here:
http://developer.android.com/training/basics/firstapp/running-app.html


---- Algortihm ----
HOW TO USE:

Typically the usage of this program would happen in the background.  The database would make an input call to the program and the program would return the correct output.

However if a user would like to manually manage the program the input commands are as follows

FLAGS:

-reserve <start> <end> <reservation type> <reservation ID>
	
	This function creates a reservation at the designated time.
	
	Reservation types are as follows:

	0) unoccupied 1) occupied 2) reserved unoccupied 3) reserved occupied

-cleaner

	This function removes old reservations.

-sort

	This function runs the sort algorithm on a previously made matrix.


OVERVIEW:
The data will be stored as integers within an array.  The algorithm will note in the array matrix where the parking reservation begins and ends.  These two integers are critical for determining where the spot can be shifted to.  The algorithm will need to check each parking spot and check if there is no conflict between the beginning and end times with any previously placed reservations.  Since the consolidation of these parking reservations is the number one goal, it is important to minimize the unused times between parking reservations.  To take this into account, a counter which is initialized to zero will be used.  

The counter is used to describe the maximum time units (here our time unit is described as 15 minute intervals)  
there can be between the end of the swapped reservation and a reservation in place or the beginning of the 
swapped reservation and end of a reservation in place.  If the algorithm cannot find a spot to place the 
reservation, then the algorithm goes onto the next reservation to begin swapping.  However, if there are available 
spots but does not meet the maximum time unit requirement, the counter will be incremented by one and the 
process repeats until the conditions are satisfied.  It it is important to note that the counter cannot increment 
more than the number of time units there were in the original reservation spot.















