# RAILWAY-DATABASE-MANAGEMENT-SYSTEM
Overview of the Dataset
Schema Description:

pid: Passenger ID (integer, unique, not null)
tid: Ticket ID (integer, primary key)
pname: Passenger Name (varchar, up to 30 characters)
ticketfare: Fare of the ticket (integer)
paymentmode: Mode of payment (varchar, up to 30 characters)
destination: Destination city (varchar, up to 30 characters)
Analysis Queries
Total Number of Passengers:
Total Revenue from Ticket Fares:
Average Ticket Fare:
Passengers Grouped by Destination:
Total Revenue by Payment Mode:
Passengers Grouped by Payment Mode:
Highest Ticket Fare:
Passengers to a Specific Destination
Average Ticket Fare per Destination:
Total Number of Reservations by Class:
Reservations Grouped by Date of Journey:
Passengers with Multiple Reservations:
Total Number of Reservations by Class:
Total Revenue by Class:
Inner Join
An inner join retrieves records that have matching values in both tables. In the context of the passenger and reservation tables, it will show only the passengers who have made a reservation.
Left Join
A left join retrieves all records from the left table (passenger), and the matched records from the right table (reservation). The result is NULL from the right side if there is no match.Right Join
A right join retrieves all records from the right table (reservation), and the matched records from the left table (passenger). The result is NULL from the left side if there is no match.
