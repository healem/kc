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

![Alt text](http://g.gravizo.com/g?
@startuml;
Actor user;
participant "Location" as A;
participant "Weather1" as B;
participant "Weather2" as C;
participant "Weather3" as D;
participant "Text File" as E;
user -> A;
Activate A;
A -> B: Check Weather;
activate B;
B -> A: Return Weather;
deactivate B;
A -> C: Check Weather;
activate C;
C -> A: Return Weather;
deactivate C;
A -> D: Check Weather;
activate D;
D -> A: Return Weather;
deactivate D;
A -> E: Print Weather From 1,2,3;
deactivate A;
activate E;
E -> user;
deactivate E;
@enduml
)


###functions

###Inputs

Location in zipcode, time interval and weather APIs

###Outputs

temperature in degrees (C or F?)

###User Interaction

Insert location and set time interval
