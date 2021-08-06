Implemented a few SQL queries

Following is the ER diagram of the data discussed for question 1:

Description of ER diagram :

ENTITIES :

STUDENT

This entity is used to store the student data
Its primary key is Student_ID(an unique 10 digit code)
It includes students first name, last name and also if the student has paid the fees(boolean)
This table can have many more attributes but we limit it according to our model
PROJECT

This table stores all the necessary information of the projects
Its primary key is a composite key (Project_ID, Student_ID). As a group of four students will have the same Project_ID, thus, alone Project_ID cannot be the primary key(as it cannot be unique)
It has attributes like Project_Name, Instructor_ID( instructor that supervises the respective project), Room_ID( Room in which the project will be held), Project_Time( schedule of the respective project)
I have made an assumption that one student has to take atleast one project
INSTRUCTOR

This table stores all the necessary information of the instructors
Its primary key is Instructor_ID(an unique 10 digit code)
It includes instructors first name, last name and also total no of hours that he has worked
4.CLASS - This entity is used to store the class data - Its primary key is (Class_ID, Student_ID). As many students can enroll for the same class, thus, Class_ID alone cannot be a primary key. - I have made an assumption that one student has to take atleast one class - It has attributes like Class_Name, Instructor_ID( instructor that supervises the teaches the resp class), Room_ID( Room in which the class will be held), Textbook_ID( textbook through which the class will be taught)

TEXTBOOK

This entity is used to store the texbook data
Its primary key is Textbook_ID(an unique 10 digit code)
It has a attribute Textbook_Name
RATING

This table stores all the necessary information of the rating at the end of the class
Its primary key is Rate_ID
Student will rate the project and the class of the resp instructor
SALARY

This entity is used to store the Salary data
Its primary key is Salary_ID(blind ID)
Its attributes are Instructor_ID, Rate( per hour rate), Total_Salary
LIBRARY

This table stores all the necessary information of the library
Its primary key is Trans_ID(Each entry for new transaction, blind ID)
Its attributes are which book(Book_ID) is issued by which student(Student_ID), issue and return date
ROOM

It give the information about the rooms
Its primary key is(Room_ID, Table_No). As one room can have multiple tables, thus, room alone cannot be primary key
It has attribute Location_ID which tells the geographical location of the room
LOCATION

It gives geographical location information
Its attributes are building name, floor and the street name
TABLE

This entity describes the the tables in the rooms
Its primary key is Table_ID( It will be unique, irrespective of the room in which it is situated)
Its attribute is Box_ID (The box which is alloted to that table)
BOX

It gives the information of the box on the tables
Its primary key is a composite key(Box_ID, Component_ID). A box can contain multiple components, thus, box alone cannot be a primary key
COMPONENTS

It gives details about component
VENDOR

Gives details about Vendor
RELATIONSHIPS:

Assumed that one student can take part in only one project
Assumed that one student can enroll in one class
Assumed that student has an option to use the library, he may or may not go to the library( zero to many)
Each transaction will definately have one student involved
I have added colours just for fun, no particular meaning
