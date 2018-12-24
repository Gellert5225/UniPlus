
# Data Model

This section contains the data model for Student, Mentor, Parent, Project, Debrief.

## Person

The base class for Student, Parent and Mentor. 

Identifier | Data Type | Description
-------------- | -------------- | -------------- 
username | String | The username for the specific user
name | String | The real name for the specific user
id | String | The object id stored in database
userGroup | String | Either a "mentor" or a "parent"
profilePhoto | Parse File | The profile picture for the specific user
parseObject | Parse Object | The Parse Object associated with the specific user

## Student

```swift
// to initialized a student object
let studentObject: PFObject = ... // retrieve student from database
let student = Student(from: studentObject)

// to retrieve total class of a program
func getTotalClass() -> Int {
return program == "STEM Club" ? 52 : 12
}
```

```java
// future Java code
```

The derived class from Person, which contains all information about a student.

Identifier | Data Type | Description
-------------- | -------------- | -------------- 
program | String | The program in which the student participates
level | String | The level of the program at which the student currently is
gender | String | The gender of the student
projectsFinished | Integer | Number of projects completed by the specific student
classesFinished | Integer | Number of classes completed by the specific student (within one program)
lastAttendance | Date | The last date which the student attends
projects | Array<[Project](#project)> | An array of projects completed by the specific student
currentProject | [Project](#project) | The project that the student is working on
day | [Day](#day) | The come-in date and time for the specific student

## Mentor

The derived class from Person, which contains all information about a mentor.

Identifier | Data Type | Description
-------------- | -------------- | -------------- 
mentorInfo | String | The information about the specific mentor
availableDates | Array<[Day](#day)> | The available date and time for the specific mentor

## Parent

The derived class from Person, which contains all information about a parent.

Identifier | Data Type | Description
-------------- | -------------- | -------------- 
phone | String | The phone number of the specific parent
email | String | The email of the specific parent
students | Array<[Student](#student)> | An array of students who belong to the specific parent

## Project

```swift
// to initialized a project object
let projectObject: PFObject = ... // retrieve project from database
let project = Project(from: projectObject)
```
```java
// future Java code
```


This class contains all information about a student's project.

Identifier | Data Type | Description
-------------- | -------------- | -------------- 
projectName | String | The name of the project
description | String | The description of the project
language | String | The programming language of the project
progress | String | Student's progress on this project
student | [Student](#student) | The student who is working on this project

<aside class="notice">The progress of a project must be set strictly(case sensitive) to "In Progress" or "Finished" or "Presented".</aside>

## Debrief

This class contains all information about a student's debrief.

Identifier | Data Type | Description
-------------- | -------------- | -------------- 
mentorName | String | The name of the mentor
description | String | The debrief content
mentor | [Mentor](#mentor) | The mentor who was working with the student
date | Date | The date which the debrief is created

## Others

Other helper data structures.

### Day

```swift
// to initialized a day object
let day = Day(from: "Monday 0900 0400")

// to convert day into String
day.toTimeString() // "Monday 0900 0400"

// to display time
print(day) // or day.description will give you "Monday 9:00 - 4:00"
```
```java
// future Java code
```


This is a structure which contains a weekday and a time range for displaying mentor availability and student attendance.

Identifier | Data Type | Description
-------------- | -------------- | -------------- 
day | String | The weekday
timeRange | Tuple | The time range in String tuple format: `((beginHour, beginMinuet), (endHour, endMinuet))`

<aside class="notice">This object will be stored as a String in the database, with the format of "Monday 0300 0800" or "Saturday 1100 0240", which mean "Monday 3 to 8 pm" and "Saturday 11am to 2:40pm" respectively.</aside>
