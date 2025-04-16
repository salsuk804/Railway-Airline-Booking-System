Railway-Airline Booking System

*********Note: This project was developed without the use of any built-in functions or advanced libraries. All logic, data handling, and control flow were implemented manually using basic programming constructs, as per the constraints of the final year project*********

Project Overview
This is a Final Year Project that implements a comprehensive Railway and Airline Booking System. The system allows users to search, book, and manage train and flight tickets through a unified console-based interface.

Assumptions:

- City of Origin: All flights and trains are assumed to operate from the city of Lahore.
- Passenger Age: Only passengers aged 18 and above are allowed to book tickets.
- Maximum Records: The system can store a maximum of 10 passenger records.
- Ticket Limit: A maximum of 5 tickets can be booked at a time for any flight or train.
- Fixed Schedules: The flight and train schedules, including departure times and costs, are predefined and do not change dynamically.
- Simple Interface: The application operates through a console interface, and user inputs are assumed to be valid (no extensive error handling).
- Deposit Requirement: Passengers must deposit an amount greater than or equal to the total cost of the tickets before confirmation.
- Cancellation Policy: All recent tickets booked by a passenger can be canceled at once, and the available seats will be reset to their maximum capacity.


Features

- Display Flights and Trains: View available options with details such as available seats, departure times, transport numbers, and ticket costs.
- Add Passenger Records: Add personal information (name, age, CNIC/passport number, contact number).
- Book Tickets: Book tickets for flights or trains based on destination and number of tickets.
- Cancel Tickets: Cancel all recent bookings and update seat availability.
- Search Passenger Records: Search using CNIC or passport number.
- Filter Options: Filter flights and trains by destination or departure time.
- Generate Report: View a report of all recent bookings made by passengers.


Code Structure

1. Main Function:

The main function contains the core logic of the application. It presents a menu-driven interface implemented using a do-while loop that continues until the user chooses to exit.

2. Data Structures:
The application uses multiple arrays to manage data for passengers, bookings, flights, and trains.


** Passenger Information Arrays:

-  passName[10]: Stores passenger names
-  passID[10]: Stores CNIC or passport numbers
-  passAge[10]: Stores passenger ages
-  passContact[10]: Stores contact numbers
-  passBalance[10]: Stores account balances, initialized to zero


** Ticket Booking Arrays:

-  recentBooking[10]: Stores recent bookings for each passenger
-  passTicktCount[10]: Tracks number of tickets booked by each passenger
  

** Flight Information Arrays:

-  PIAseats[3]: Tracks available seats for Pakistan International Airline
-  FlyJinnahSeats[3]: Tracks available seats for Fly Jinnah
-  PIA_Cities[3]: Stores destination cities for PIA flights
-  FLY_J_Citites[3]: Stores destination cities for Fly Jinnah flights
-  PIA_Cost[3]: Stores ticket costs for PIA flights
-  FLY_J_Cost[3]: Stores ticket costs for Fly Jinnah flights
-  PIA_FlightNumbers[3]: Stores flight numbers for PIA
-  FLY_J_FlightNumbers[3]: Stores flight numbers for Fly Jinnah
-  PIA_Departure[3]: Stores departure times for PIA flights
  

** Train Information Arrays:

-  PakExpress_Seats[3]: Tracks available seats for Pakistan Express trains
-  FastExpress_Seats[3]: Tracks available seats for Fast Express trains
-  PakExpress_Cities[3]: Stores destination cities for Pakistan Express
-  FastExpress_Cities[3]: Stores destination cities for Fast Express
-  PakExpress_Cost[3]: Stores ticket costs for Pakistan Express trains
-  FastExpress_Cost[3]: Stores ticket costs for Fast Express trains
-  PakExpress_TrainNumber[3]: Stores train numbers for Pakistan Express
-  FastExpress_TrainNumner[3]: Stores train numbers for Fast Express
-  PakExpress_Departure[3]: Stores departure times for Pakistan Express trains


3. Control Flow:

The program operates using a do-while loop to continuously display the main menu until the user exits. Menu options are handled using if and else if conditions.


4. Key Variables:

- counter: Tracks the number of passengers added
- choice: Stores the user's main menu selection
- transportChoice: Stores the user's choice between airline or train
- AirLineChoice: Stores selected airline
- TrainChoice: Stores selected train
- y: Tracks the number of recent bookings

*** Functionality Breakdown:

Main Menu Options: 

1. Display all Flights and Trains
2. Add Passenger Record
3. Book Tickets
4. Cancel Tickets
5. Search Passenger Record
6. Filter Flights and Trains
7. Generate Report
8. Exit


Display Flights and Trains:

  Displays transport options with the following details:

- Destination City
- Available Seats
- Departure Time
- Flight/Train Number
- Ticket Cost


Add Passenger Record:

Prompts the user to input:
Name
Age (must be 18 or older)
CNIC or Passport Number
Contact Number


Book Tickets:

Select transport type (airline/train)
Select destination and number of tickets
Check seat availability
Deposit an amount ≥ total cost
Confirm booking and update seat count


Cancel Tickets:

Cancels all recent bookings from the recentBooking[] array
Resets seat availability to max for each canceled booking
Clears the record of recent bookings


Search Passenger Record:

Allows users to search using their CNIC or passport number and displays:
Passenger Name
Booking Details


Filter Flights and Trains:

Filter by:
Destination
Departure Time
Displays matching results based on user input.


Generate Report:

Displays all recent bookings, including:
Passenger Names
Number of Tickets
Booking Summary








