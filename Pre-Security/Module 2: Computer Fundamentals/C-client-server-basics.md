# C. Client-Server Basics

## Client-Server Model

The **client-server model** is a network architecture where a client requests a service and a server provides the requested service.

```text
Client  ─────── Request ───────>  Server
Client  <────── Response ───────  Server
```

A client initiates communication with the server, and the server responds to the client's request.

---

## Client

A **client** is a network application that requests a service.

### Examples

- Web browser
- SSH client
- Email client
- FTP client

A client sends requests to a server and receives the requested service or resource in response.

---

## Server

A **server** is a system, application, or service that provides a service or resource to clients.

A single computer can run multiple servers/services simultaneously.

### Examples

- Web server
- DNS server
- Mail server
- SSH server
- FTP server

The server receives requests from clients, processes them, and sends back a response.

---

## Request and Response

Client-server communication follows a **request-and-response** model.

### Request

A **request** is sent by the client to ask the server for a resource or service.

```text
Client → Request → Server
```

### Response

A **response** is sent by the server after processing the client's request.

```text
Server → Response → Client
```

The response is divided into two parts:

- **Response Header** → contains metadata about the response.
- **Response Body** → contains the requested content.

```text
Response
├── Response Header
└── Response Body
```

## Protocol

A **protocol** is a set of rules that defines how computers communicate.

It specifies:

- What commands are understood
- How requests are structured
- What syntax should be used
- What the response should look like
- How communication is controlled

---

## Port

A **port** is used to identify a particular network service.

A port is a logical endpoint that allows a specific service to communicate over a network.

A port number is used to access a particular service.

---

## DNS

**DNS (Domain Name System)**

It is the protocol responsible for resolving hostnames to their respective IP addresses.

---

## HTTP(S)

- **HTTP** → Hypertext Transfer Protocol
- **HTTPS** → Hypertext Transfer Protocol Secure

HTTP(S) is a **client-server protocol** used primarily for communication on the World Wide Web.

It is a **stateless protocol**, i.e. the server does not inherently remember previous requests made by the client. Each request is treated as an independent request.

---

## HTTP Request Methods

HTTP uses methods to indicate what the client wants to do.

### a) GET

- Used to retrieve data from a server.
- In the Inspect tab → Network section → in the right-hand panel:

  - **Scheme** → tells us which protocol was used (HTTP/HTTPS)
  - **Host** → tells us the name of the host we request resources from
  - **Filename** → indicates which file we requested from the host
  - **Address** → displays the IP address where the website is hosted
  - **Status** → indicates whether the request was successful

When a request is sent, we will get a response from the server.

The response is divided into two parts:

- **Response Header** → contains metadata about the response
- **Response Body** → contains the requested content

### b) POST

- It is generally used to send data to a server.
- Common uses:
  - Login forms
  - Creating accounts
  - Submitting forms
  - Uploading data

  ### c) PUT

- It is generally used to create / completely replace a resource at a specified location.

### d) DELETE

- It requests the server to delete a resource.

### e) PATCH

- It is used to partially modify an existing resource.
- **PUT** → replaces / updates the whole resource
- **PATCH** → modifies part of the resource

### f) HEAD

- It works similarly to GET, but the server returns the response headers without the response body.
- Useful for checking information such as:
  - Whether a resource exists
  - Content-Type
  - Content-Length
  - Last modification information
- This can be done without downloading the actual content.

### g) OPTIONS

- It asks the server what communication options / methods are available for a resource.

### h) CONNECT

- It is used to establish a network tunnel to the server.

### i) TRACE

- It is primarily a diagnostic method.
- It asks the server to return the request it received, allowing the client to see how the request was processed through the HTTP infrastructure.
- It is generally disabled on production servers because of security considerations.

---

## Note

- HTTP is also called **Request for Comments (RFC)** documents.
- **RFC** is a publication in a series from the principal technical development and standards-setting bodies for the Internet, most prominently the **Internet Engineering Task Force (IETF)**.
