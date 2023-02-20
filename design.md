# Design Document: Vacation Tracker

This is my first database design. In order to keep things simple, I am starting with a vacation/holiday/sick tracker for work. Once the database is working, I might take the next step of creating a web interface for entering data and running reports.

I know I will make tons of mistakes but I expect that I will learn a ton through this project. I will be able to apply my learning to the next databases I want to design.

Here are the steps that I expect to take in this project:

* envision the information I want to get out of this database
    * I expect this will help me immensely in figuring out the next steps
* determine information to be stored in the tables
* determine relation between table items
* construct the database
* load data into the database

## Database Outputs

The purpose of this database is to answer the following questions:

* How many vacation/holiday/sick hours/days have I taken so far this year?
* How many vacation/holiday/sick days/weeks do I have left this year?
* How many vacation hours/days must I take before the end of the year?
* How many vacation hours/days am I starting & ending the year with?
* How did I use the vacation time on each calendar day?
* When did I take each vacation/holiday/sick hour/day?

Minimum value to measure: 0.25 hour

At first I will gather this information from a command line query. Over time, I would like to add this information to a dashboard that is viewable at home, work, or on my phone.

## Information Needed

### Table Name: day_types

Contains information about the different types of hours/days that I am tracking: vacation, holiday, sick

dayTypeId
dayType (vacation, holiday, sick, non-paid leave)

### Table Name: holidays

This is a listing of the holidays designated by my workplace. It will change each year based on where the holidays fall in the calendar week - this will probably require another table.

holidayId
holidayName
holidayDate

### Table Name: hours_taken

I will track how many hours of time I have taken off each day. It's not important to know when my time off started or ended - only how many hours total I took off each day.

I also want to plan days off. This way I can plug in a planned vacation to determine how it will affect my balance for the remainder of the year.

hoursTakenId
hoursTakenNumber
hoursTakenDate
hoursPurpose
hoursStatus

Need to also consider starting hour value & monthly/annual addition of hours


Table Name: 
Table Name: 

