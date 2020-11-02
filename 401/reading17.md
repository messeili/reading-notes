# Reading17: TCP Servers

## Review, Research, and Discussion

- **Given the examples of front-end events such as button click, window resize, form submit, etc, what are some examples of back-end events?**
- **Why are events sometimes better than asynchronous actions with callbacks?** Generally speaking, a 'callback' is under the control of the detecting process. So you tell a GUI manager "call myaction when this button is pressed" and the GUI manager calls the action when the button is pressed.Event Handlers on the other hand operate at one step removed. The GUI manager is configured to send messages to an event handler. You tell an event manager that button pushes are handled by the myaction program. When the button is pushed the GUI manager puts a message on the event handler's queue and gets on with GUI managing. The event handler picks up the message from the queue, sees it's a button push, fires up the myaction program, and moves on to handling the next event. Usually the myaction program will run as an independent thread or even a separate process.
- **What does an EventEmitter instance do?** emit custom events synchronously or asynchronously, and register handlers for those events by subscribing to an instance
- **When is a program’s call stack, event queue, and event loop active?** to define the capabilities of each user

## Terms

**Observer Pattern** is a software design pattern in which an object, called the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods
**Listener** is a procedure or function in a computer program that waits for an event to occur.
**Event Handler** Any function or object that is registered to be notified of events.
**Event Driven Programming** is when a program is designed to respond to user engagement in various forms.
**Event Loop** is a programming construct or design pattern that waits for and dispatches events or messages in a program
**Event Queue** is a repository where events from an application are held prior to being processed by a receiving program or system.
**Call Stack** call stack is a stack data structure that stores information about the active subroutines of a computer program.
**Emit/Raise/Trigger**
**Subscribe** to turn the event listener on so when the listener is emited the handler will executes
**database** is a collection of information that is organized so that it can be easily accessed, managed and updated.

**Authorization** is a security mechanism to determine access levels or user/client privileges
**Role Based Access Control** is a policy-neutral access-control mechanism defined around roles and privileges.
**Capabilities** rules based on users roles.

## Preview: Event Driven Programming

##### TCP (Transmission Control Protocol)

TCP (Transmission Control Protocol) is a standard that defines how to establish and maintain a network conversation through which application programs can exchange data. TCP works with the Internet Protocol (IP), which defines how computers send packets of data to each other. Together, TCP and IP are the basic rules defining the Internet. The Internet Engineering Task Force (IETF) defines TCP in the Request for Comment (RFC) standards document number 793.

##### The OSI model

The Open Systems Interconnection (OSI) model is a conceptual model created by the International Organization for Standardization which enables diverse communication systems to communicate using standard protocols. In plain English, the OSI provides a standard for different computer systems to be able to communicate with each other.

The OSI model can be seen as a universal language for computer networking. It’s based on the concept of splitting up a communication system into seven abstract layers, each one stacked upon the last.
![img50](https://www.cloudflare.com/img/learning/ddos/what-is-a-ddos-attack/osi-model-7-layers.svg)

##### Example of TCP server in Node.js:

TCP Server:

```
'use strict';

// load the Node.js TCP library
const net = require('net');
const PORT = 1234;
const HOST = 'localhost';

class Server {
constructor(port, address) {
this.port = port || PORT;
this.address = address || HOST;

this.init();
}

init() {
let server = this;

let onClientConnected = (sock) => {

let clientName = `${sock.remoteAddress}:${sock.remotePort}`;
console.log(`new client connected: ${clientName}`);

sock.on('data', (data) => {
console.log(`${clientName} Says: ${data}`);
sock.write(data);
sock.write('exit');
});

sock.on('close', () => {
console.log(`connection from ${clientName} closed`);
});

sock.on('error', (err) => {
console.log(`Connection ${clientName} error: ${err.message}`);
});
}

server.connection = net.createServer(onClientConnected);

server.connection.listen(PORT, HOST, function() {
console.log(`Server started at: ${HOST}:${PORT}`);
});
}
}
module.exports = Server;
```

To test server, use following code in another file and run it
` const Server = require('./server'); new Server();`

TCP Client:

```
'use strict';

const net = require('net');
const PORT = 1234;
const HOST = 'localhost';

class Client {
constructor(port, address) {
this.socket = new net.Socket();
this.address = address || HOST;
this.port = port || PORT;
this.init();
}
init() {
var client = this;

client.socket.connect(client.port, client.address, () => {
console.log(`Client connected to: ${client.address} : ${client.port}`);
client.socket.write('Hello World!');
});

client.socket.on('data', (data) => {
console.log(`Client received: ${data}`);
if (data.toString().endsWith('exit')) {
client.socket.destroy();
}
});

client.socket.on('close', () => {
console.log('Client closed');
});

client.socket.on('error', (err) => {
console.error(err);
});

}
}
module.exports = Client;
```

To test client, use following code in another file and run it
`const Client =require('./client'); new Client();`
Output:

Server:

```
D:\node>node serverTest.js Server started at: localhost:1234 new client connected: 127.0.0.1:62846 127.0.0.1:62846 Says: Hello World! connection from 127.0.0.1:62846 closed
```

Client:

```
D:\node>node clientTest.js Client connected to: localhost : 1234 Client received: Hello World! Client received: exit Client closed
```
