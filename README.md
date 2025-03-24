Observer Pattern Implementation
Overview
This project demonstrates the Observer Design Pattern in Java. The pattern is used to establish a one-to-many dependency between objects, ensuring that when one object (the subject) changes state, all its dependents (observers) are automatically notified and updated.

Files and Classes
Observer.java: Abstract class defining the observer interface.
Subject.java: The subject that maintains a list of observers and notifies them of state changes.
BinaryObserver.java: Concrete observer that represents the state in binary format.
HexaObserver.java: Concrete observer that represents the state in hexadecimal format.
OctalObserver.java: Concrete observer that represents the state in octal format.
ObserverPatternDemo.java: Main class demonstrating the observer pattern in action.
How It Works
The Subject class maintains a list of observers and provides methods to attach, detach, and notify them.
Concrete observer classes (BinaryObserver, HexaObserver, OctalObserver) extend Observer and implement the update method to respond to state changes.
In ObserverPatternDemo.java, a Subject object is created, and multiple observers are attached to it.
Changing the Subject's state triggers notifications to all attached observers, displaying the state in different formats.
The demo also includes an SMS listener component, though its functionality is separate from the main observer pattern.
Example Output
First state change: 15
Hex String: F
Octal String: 17
Binary String: 1111
Second state change: 10
Hex String: A
Octal String: 12
Design Pattern Used
Observer Pattern: Enables loose coupling between the subject and its observers, making the system more modular and maintainable.
