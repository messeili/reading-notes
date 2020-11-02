# Reading14: Access Control (ACL)

## Review, Research, and Discussion

## Review, Research, and Discussion

- What is the benefit of transforming data into packets?

Packet switching with its supporting packet processing functions has several practical benefits over traditional circuit-switched networks

- UDP is often refereed to as a connection-less protocol. Why is this?

No connection needs to be established between the source and destination before you transmit data

- Can a socket server application have multiple socket connections?

Can share the same server-side IP/Port pair as long as they are associated with different client-side IP/Port pairs

- Can a socket connection application be connected to multiple socket servers?

Yes, you need a separate connection factory for each server/port.

- Can an application be both a socket server and a socket connection?

Yes, it can.

##Terms

- **OSI Model**: conceptual framework used to describe the functions of a networking system.
- **TCP Model**: conceptual model and set of communications protocols used in the Internet and similar computer networks.
- **TCP**: one of the main protocols of the Internet protocol suite.
- **UDP**: communications protocol that is primarily used for establishing low-latency and loss-tolerating connections between applications on the internet.
- **Packets**: formatted unit of data carried by a packet-switched network.
- **Socket**: software structure within a network node of a computer network that serves as an endpoint for sending and receiving data across the network.

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

##### Difference Between WebSocket and Socket.io

WebSocket is the communication Protocol which provides bidirectional communication between the Client and the Server over a TCP connection, WebSocket remains open all the time so they allow the real-time data transfer. When clients trigger the request to the Server it does not close the connection on receiving the response, it rather persists and waits for Client or server to terminate the request.

Socket.IO is a library which enables real-time and full duplex communication between the Client and the Web servers. It uses the WebSocket protocol to provide the interface. Generally, it is divided into two parts, both WebSocket vs Socket.io are event-driven libraries
