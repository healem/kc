#Weather Checker

##Intro

###Purpose

Get the current temperature from 3 different weather sites every 5 minutes and write the results to a single file

###Scope

* Creating a Java application that is multi-threaded and shares a resource
* A Java app that writes to a file
* A Java app that Accesses a web services API
* Getting more comfortable with git

###Class Diagram

<img src='http://g.gravizo.com/g?
@startuml;

Package "Java App"{
Main - timeInterval : <output;
Main - location : <output;
Main : timeInterval;
Main : location;
timeInterval : int minutes : 5;
location : zipCode : 06787;
}
Main - Text :output;
package "Outside API"{
Main - Weather1: Temp;
Main - Weather2: Temp;
Main - Weather3: Temp;
}
@enduml;
'>

###Sequence Diagram
![image of sequence diagram]
(http://www.plantuml.com:80/plantuml/png/XP6n2eCm443tVCNXR0Vhvb28IPmwb5Be7D83GrkLU9P-VasqhOBY5lBUlOI46weTT2qwrcX7rjX6LmJHiJQQR5r5e5lWStP5JIMw9B1yaUq34uii3KpEsGNV18LzO82A-Hl1xj0VpGtPboRqIx-JPo1AD7SOSqn_XPpbOII3CrBdgfznmuaJ8c8r8fZOZ8WX8bSZaidDY1mYAeEJi_qJZ0eKhdv24k_ZT6hpVrmnvGV3dqqCzG40)

###functions

###Inputs

Location in zipcode, time interval and weather APIs

###Outputs

temperature in degrees (C or F?)

###User Interaction

Insert location and set time interval
