# Reading19: Message Queues

## Review, Research, and Discussion

- **What does it mean that web sockets are bidirectional? Why is this useful?**
- **Does socket.io use HTTP? Why?** yes, because both http and webSocket are TCP connections
- **What happens when a client emits an event?** it will look for event listener inside the server and trigger it.
- **What happens when a server emits an event?** it will look for event listener inside the server then will be broadcasting that event for all clients.
- **What happens if a client “misses” an event?**
- **How can we mitigate this?**

## Terms

- **Web Socket** is a computer communications protocol, providing full-duplex communication channels over a single TCP connection.
- **Socket.io** is a JS library that allows bi-directional communication between client and server
- **Client**
- **Server**

## Preview

##### Socket.IO

Socket.IO is a JavaScript library for real-time web applications. It enables real-time, bi-directional communication between web clients and servers. It has two parts: a client-side library that runs in the browser, and a server-side library for node.js. Both components have an identical API.

Real-time applications
A real-time application (RTA) is an application that functions within a period that the user senses as immediate or current.

Some examples of real-time applications are −

Instant messengers − Chat apps like Whatsapp, Facebook Messenger, etc. You need not refresh your app/website to receive new messages.

Push Notifications − When someone tags you in a picture on Facebook, you receive a notification instantly.

Collaboration Applications − Apps like google docs, which allow multiple people to update same documents simultaneously and apply changes to all people's instances.

Online Gaming − Games like Counter Strike, Call of Duty, etc., are also some examples of real-time applications.
