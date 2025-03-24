# Observer Pattern Implementation

## Overview
This project demonstrates the **Observer Design Pattern** in Java. The pattern is used to establish a one-to-many dependency between objects, ensuring that when one object (the subject) changes state, all its dependents (observers) are automatically notified and updated.

## Files and Classes
- **Observer.java**: Abstract class defining the observer interface.
- **Subject.java**: The subject that maintains a list of observers and notifies them of state changes.
- **BinaryObserver.java**: Concrete observer that represents the state in binary format.
- **HexaObserver.java**: Concrete observer that represents the state in hexadecimal format.
- **OctalObserver.java**: Concrete observer that represents the state in octal format.
- **ObserverPatternDemo.java**: Main class demonstrating the observer pattern in action.
- **SMSSupportListener.java**: A listener that checks the length of received SMS messages and warns if they exceed 100 characters.
- **SMSReceiver.java**: A receiver that takes incoming SMS messages and passes them to the listener for processing.

## How It Works
1. The `Subject` class maintains a list of observers and provides methods to attach, detach, and notify them.
2. Concrete observer classes (`BinaryObserver`, `HexaObserver`, `OctalObserver`) extend `Observer` and implement the `update` method to respond to state changes.
3. In `ObserverPatternDemo.java`, a `Subject` object is created, and multiple observers are attached to it.
4. Changing the `Subject`'s state triggers notifications to all attached observers, displaying the state in different formats.
5. The `SMSSupportListener` class checks if an SMS message exceeds 100 characters and prints a warning if necessary.
6. The `SMSReceiver` class receives SMS messages and passes them to the `SMSSupportListener` for validation.

## How to Run
1. Compile all Java files:
   ```sh
   javac *.java
   ```
2. Run the main class:
   ```sh
   java ObserverPatternDemo
   ```
3. The output will show state changes and their representations in binary, octal, and hexadecimal, along with SMS validation messages.

## Example Output
```
First state change: 15
Hex String: F
Octal String: 17
Binary String: 1111
Second state change: 10
Hex String: A
Octal String: 12
Receiving SMS: This is a long SMS message that exceeds the 100 character limit...
Warning: SMS content exceeds 100 characters!
Receiving SMS: Short SMS.
SMS content is within the acceptable length.
```

## Design Pattern Used
- **Observer Pattern**: Enables loose coupling between the subject and its observers, making the system more modular and maintainable.


