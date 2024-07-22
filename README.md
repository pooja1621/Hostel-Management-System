# Hostel-Management-System
Hostel management system using C++


Here's a detailed description of the Hostel Accommodation System implemented in C++:

Hostel Accommodation System
Overview
The Hostel Accommodation System is a console application written in C++ that manages hostel bed reservations. It allows users to reserve a bed in a hostel and maintains records of students who have reserved the beds. This system also supports viewing and updating of bed availability in a hostel.

Components
1. Hostel Class
Attributes:

Name: Name of the hostel.
Rent: Monthly rent for a bed in the hostel.
Bed: Number of available beds.
Methods:

Constructor: Initializes the hostel's name, rent, and number of beds.
getName(): Returns the name of the hostel.
getRent(): Returns the rent amount.
getBed(): Returns the number of available beds.
reserve(): Manages the bed reservation. It reads the hostel data from a file (D:/Hostel.txt), updates the number of available beds, and writes the updated data to a temporary file which replaces the original file after updating.
2. Student Class
Attributes:

Name: Student's name.
RollNo: Student's roll number.
Address: Student's address.
Methods:

Constructor: Initializes the student's attributes to empty strings.
setName(string name): Sets the student's name.
setRollNo(string rollNo): Sets the student's roll number.
setAddress(string address): Sets the student's address.
getName(): Returns the student's name.
getRollNo(): Returns the student's roll number.
getAddress(): Returns the student's address.
3. Main Function
The main function provides an interactive menu for users to manage hostel reservations:

Initial Setup:

Creates an instance of the Hostel class with predefined values.
Saves the initial hostel data to a file (D:/Hostel.txt).
Menu Options:

Option 1: Reserve A Bed:
Prompts the user for student details (name, roll number, and address).
Checks if there are available beds in the hostel.
If beds are available, it reserves a bed by updating the file and saves the student's details to another file (D:/Student.txt).
If no beds are available, it notifies the user.
Option 2: Exit:
Exits the application.
Features
Dynamic Bed Reservation: The system updates the number of available beds in real-time by modifying the data file.
Student Record Management: Student details are appended to a file each time a reservation is made.
User Interaction: The console interface allows users to interact with the system using a simple menu.
Error Handling
File Operations: The system handles file operations for reading and writing hostel and student data. Ensure that the paths (D:/Hostel.txt and D:/Student.txt) are correctly set up and accessible.
Limitations
File Path Assumptions: The application uses absolute paths which may not work on different systems. Modify file paths as needed.
Concurrency: The system does not handle concurrent access, meaning simultaneous reservations could cause issues if multiple instances of the program are run.

