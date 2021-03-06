--- 
title: "Activity Diagram"
date: 2021-02-15T21:43:46+01:00 # update date !

draft: false # toggle to false when final version is approved !

languageName: "English"
author: ["Massimo", "Riccardo", "Gabriele", "Francesco"] 

tags: ["Software Requirements"]
categories: ["Software Requirements"]         
---  


---
An activity diagram is an important behavioral diagram in UML used to describe the dynamic aspects of a system. 
Activity diagrams are essentially an advanced version of a flowchart that models the flow from one activity to another. 

&nbsp
### When to Use Activity Diagrams?

Activity Diagrams describe how activities are coordinated to provide a
service which can be at different levels of abstraction. Typically, an event
needs to be achieved by some operations, particularly where the
operation is intended to achieve a number of different things that require
coordination, or how the events in a single use case relate to one
another, in particular, use cases where activities may overlap and require
coordination. It is also suitable for modeling how a collection of use cases
coordinate to represent business workflows.

- Identify candidate use cases, through the examination of business workflows
- Identify pre- and post-conditions (the context) for use cases
- Model workflows between/within use cases
- Model complex workflows in operations on objects
- Model in detail complex activities in a high level activity Diagram

&nbsp
### Difference between an Activity diagram and a Flowchart

Flowcharts were typically invented earlier than activity diagrams. Non
programmers use Flow charts to model workflows. For example: A
manufacturer uses a flow chart to explain and illustrate how a particular
product is manufactured. We can call a flowchart a primitive version of an
activity diagram. Business processes where decision making is involved is
expressed using a flow chart.

&nbsp
### Construction

Activity diagrams are constructed from a limited number of shapes,
connected with arrows. The most important shape types:

- Ellipses represent actions;
- Diamonds represent decisions;
- Bars represent the start (split) or end (join) of concurrent activities;
- A black circle represents the start (initial node) of the workflow;
- An encircled black circle represents the end (final node).
- Arrows run from the start towards the end and represent the order in which activities happen.

&nbsp 
### Structure of an Activity Diagram
&nbsp

![Activity Diagram Structure](/images/ActivityDiagram/1.png) 

&nbsp
### Activity Diagram - Modeling a Word Processor (Example)

The activity diagram example below describes the workflow for a word process to
create a document through the following steps:

- Open the word processing package.
- Create a file.
- Save the file under a unique name within its directory.
- Type the document.
- If graphics are necessary, open the graphics package, create the graphics, and paste the graphics into the document.
- If a spreadsheet is necessary, open the spreadsheet package, create the spreadsheet, and paste   the spreadsheet into the document.
- Save the file.
- Print a hard copy of the document.
- Exit the word processing package.

&nbsp
### Example graph:
&nbsp

![Activity Diagram Graph](/images/ActivityDiagram/2.png)




