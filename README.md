Implement the following system using 

Assignment1: a linked list of structures 
Assignment2: any kind of tree data structure 

where every node of that list represents a record of 
    passenger name,
    passenger id, (key)
    boarding train, 
    boarding station, 
    travelling class(Sleeper, 3AC, 2AC, 1AC), /
    destination station,
    train id, 
    Seat number (bogie number/seat number), and #will be decided by program 
    any other field you think that would be useful to passengers. 
    confirmation from the passenger whether upgrade of travel class is desired/

You can also take a confirmation from the passenger whether upgrade of travel class is desired. 
The passenger id can be thought as a key in the list and will represent a unique record in the 
list. The records should be always kept sorted according to the train id so that passengers
boarding the same train have their data together.

The records should be always kept sorted according to the train id so that passengers
boarding the same train have their data together

You can assume number of bogies of each class and number of seats in each bogie. 
Write the following functions :
-insert
    • Insert a list of passengers and their details for the reservation
    • I/p parameters: Reservation request that includes a list of passenger names, 
    passenger ids, boarding train, boarding station, travelling class(Sleeper, 3AC, 
    2AC, 1AC), destination station, train id
    • O/P: Reservation done successfully, partially or the reservation failed.
    • Note – The set of passengers in a single reservation request should be 
    allocated seats together. If all of them cannot get the seats together, then they 
    need to be accommodated as close to each other in trains, that is, their 
    bogie/seat numbers should be as close to each other. 
-delete
    • Deletes an element if the passenger cancels the reservation.
    • I/p parameters: deleting all records of that particular passenger id.
    • O/p: If node gets deleted print Reservation cancelled successfully or if it gets 
    failed then print Reservation Cancellation failed.
-getListDestination
    • Get the list of passengers having the same destination station and same train id
-SortByTravelDate
    • Input – Passenger id 
    • Output – Display the list of destination stations for a particular passenger as 
    per the dates of the travel
-SortTrains
    • I/p parameters: The train database that is the linked list with passenger data as 
    given
    • O/p: Display the train number and the travel date in the sorted order of number 
    of passengers on the train. 
- PromotePassengers 
    • Input – Train id and date of travel
    • Output – For all the passengers on the train with train id and a particular date, 
    passengers can be promoted to next travel class (Sleeper -> 3AC -> 2AC ->1AC) if 
    seats are available. Passengers who had given consent for promotion to next class are 
    considered in the order of their date of booking. Note that if 2AC passenger is 
    promoted to 1AC, his/her 2AC seat becomes vacant and can be occupied by another 
    passenger from lower class under promotion.