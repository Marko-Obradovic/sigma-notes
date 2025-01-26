# HTTP

**Hyper Text Transfer Protocol**

A standardised way that we can send information between computers (more specifically between web servers and clients)

Made of four major component parts. (what are they?)

Clients and Servers speak to each other by interacting through a series of **Requests** and **Responses**. Each pair of requests and responses are made up of the following components:

1. URL - A location that a server is living at on the internet
2. Headers - Essential information about the information you're sending
3. Methods - The kind of action you want the information to trigger
5. Status Codes - A code to help you work out if the request has been successful and if not, why
6. The Body - Finally, the information you're looking to send or receive.

Everything on the internet is coordinated by a series of requests and responses between different computers. Imagine the following scenario where I am searching on Google:

HTTP is stateless. Every request is completely independant. When you make one request visiting a website, then reloading a page, going back etc, it doesn't remember anything about each individual request.

Programming, Local Storage, Cookies, Sessions are used to create enhanced user experiences.

**HTTPS - Hyper Text Transfer Protocol**

Data sent is encrypted using SSL / TLS

You need to install certificate on web host


Main HTTP  Methods:

**GET**
Retrieves data from the server

**POST**
Submits data to the server

**PUT**
Creates or overwrites data already on the server

**DELETE**
Deletes data from the server

**PATCH**
Updates PART of data already on the server

**HEAD**
Retrieves metadata of an endpoint without retrieving the content itself

![[Pasted image 20250120174639.png]]

**HTTP/2**

- Revision of HTTP
- Under the hood changes
- Respond with more data
- Reduce latency by enabling full request and response multiplexing
- Fast, efficient and secure

![[Pasted image 20250120175215.png]]

The network tab in inspect element shows all requests being made.

Clicking on each of the lines in the result will reveal all of the request headers and responses for each of the requests.

When you're inspecting each of these request and responses you'll begin to see common attributes come out of each one, for example

HTTP Request Method
Response Code
Response Headers

Use Postman to test the APIs that you're building