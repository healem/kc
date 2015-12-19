#Weather Checker

##Intro

###Purpose

Get the current temperature from 3 different weather sites every 5 minutes and write the results to a single file

###Scope

*Creating a Java application that is multi-threaded and shares a resource
*A Java app that writes to a file
*A Java app that Accesses a web services API
*Getting more comfortable with git

##System Overview

![Alt text](http://g.gravizo.com/g?
@startuml;
Package "Java App"{
Main - timeInterval : <output
Main - location : <output
Main : timeInterval
Main : location
timeInterval : int minutes : 5
location : zipCode : 06787
}
Main - Text :output
package "Outside API"{
Main - Weather1: Temp
Main - Weather2: Temp
Main - Weather3: Temp}
@enduml;
)

##System Architecture

###Functions

###Inputs and Outputs

###User interaction

###Class Diagram

###Sequence Diagram
