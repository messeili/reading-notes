# Reading16: Event Driven Applications

## Review, Research, and Discussion

- **Why is access control important?** to minimize the risk of unauthorized access to physical and logical systems.
- **What does the JSON Web Token package do?** It works this way: the server generates a token that certifies the user identity, and sends it to the client.
- **Describe an application that would need access control** school or university application which will need a separated dashboards for students and teachers.
- **What is a role used for?** to define the capabilities of each user
- **Why is role based access control more scalable than discretionary or mandatory access control?** Role Based Access Control (RBAC), also known as Non discretionary Access Control, takes more of a real world approach to structuring access control. Access under RBAC is based on a user's job function within the organization to which the computer system belongs.

## Terms

**Authorization** is a security mechanism to determine access levels or user/client privileges
**Role Based Access Control** is a policy-neutral access-control mechanism defined around roles and privileges.
**Capabilities** rules based on users roles.

## Preview: Event Driven Programming

##### EventEmitter

Node.js natively provides us with a useful module called EventEmitter that allows us to get started incorporating Event-Driven Programming in our project right away. Of course, creating our own version of EventEmitter wouldn’t be much of a challenge, and in fact there are several modules published on npm such as EventEmitter2 and EventEmitter3 which promise a faster performance than the native EventEmitter.

Those are both worth checking out if your project needs to run faster than EventEmitter will allow. They are both built to allow for syntax that is almost identical to what we’ll use for EventEmitter so learning one will make it easy to work with all of them.

We access the EventEmitter class through the events module. Once imported we’ll need to create a new object from the class to start using it.

```
const EventEmitter = require('events').EventEmitter;
const myEventEmitter = new EventEmitter;
```

##### Removing Listeners

There will likely come a time when you want to remove an event listener from an event. This could be for performance reasons (the event is no longer needed) or to avoid memory leaks (if an event listener references an object that is no longer needed, it won’t be able to be garbage-collected. This can lead to a build up of unnecessary objects).

To remove event listeners in EventEmitter we can use the removeListener or removeAllListeners method. It’s important to note that in the EventEmitter that comes built-in with Node you must pass a reference to the exact function you wish to remove when using the removeListener method. This means wherever you wish to remove the event, you’ll need to make sure the function is able to be referenced from that place in your code. For this reason it is often best to name your event handling functions and declaring them before you register the event listener, as opposed to leaving them anonymous.

```
const EventEmitter = require('events').EventEmitter;
const chatRoomEvents = new EventEmitter;

function displayMessage(message){
  document.write(message);
}

function userJoined(username){
  chatRoomEvents.on('message', displayMessage);
}

chatRoomEvents.on('userJoined', userJoined);
```

##### Object Oriented Programming + Event-Driven Programming

The last thing I want to touch on here is the combination of the Object Oriented and Event-driven programming paradigms. These two make for a very valuable combination in a wide variety of situations and I think it can be beneficial to understand and conceptualize why.

The Object Oriented approach promotes the idea that all behavior of an individual unit (or object) be handled from code within that unit. Using this approach, applications are built with many different units that all speak to and interact with each other.
