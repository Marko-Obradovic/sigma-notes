
What is an API (Application Programming Interface)?
- Set of rules and protocols for building and integrating application software. 
- Intermediary between two software applications
	- Allows different pieces of software to communicate with each other. 
- All APIs should have docs explaining the rules/endpoints
- Defines the methods and endpoints that a client can use to interact with a service.
- "Why couldn't we just access the data directly from the frontend? Or not use APIs?"
	- APIs work as a gatekeeper to data / software access. This is prevents unauthorised access to private data and accidental deletion of critical information.
	- They define the rules that programmers must follow to interact with data, software libraries, and tools - we will write ones that deal with CRUD applications. 
- How to make an API:
	- Since we're using Python, we will use frameworks like:
		1. Flask
		2. Django
		3. FastAPI
		These are "web frameworks" - meaning they're frameworks that support the development of web applications.
		- Used to avoid having to do a lot of low level application management (like dealing with protocols, or web socket management)
		- Makes it simpler for web developers to create backend APIs.
		WE USE FLASK - a lightweight web framework - works great without too much config.
- Example:
	Instead of writing all the complex code to fetch weather data from a remote server, you might use an API like weatherAPI.getTemperature(location)

What is a client?
- A client is the part of a system that makes requests to a server, then processes the response to get it back
	1. Client sends a request to the API
		- Give me the weather data for New York
	2. API processes the client's requests and sends back a response. Response contains:
		- The data the client asked for
		- A status code
	3. The client processes the data it received from the API:
		- The weather app (the client) might display the current temperature to the user based on the API's response.
- Types of clients:
	1. Web browsers (front end clients)
	2. Mobile or Desktop Applications
- client doesn't do anything until it wants to make a request
- any computer can act as a client because it can ask for requests

What is a Server?
- A machine (either hardware or software) that hosts and manages resources, services, or data.
	- Primary role: to respond to requests made by clients (like a browser, mobile app, etc)
	- Can host websites, files, or APIs
	- Listens for requests from clients (like an API request, a web page request, etc.) and returns responses
	- A machine isn't always a server - it can be a server when it needs to be, otherwise its a client if it needs to make a request
- Examples:
	- A web server (hosts a website - when you visit a URL, the browser (the client) sends a request to the server and the server responds by sending the web page back to your browser)
	- An email server could handle sending, receiving, and storing emails.


Rest API:
- (representational state transfer) a standardised software architecture style
	- A set of rules and conventions for building and interacting with web services.
	- Allows different software applications to communicate with each other over the web using standard HTTP methods

three main principles of REST APIs:
- Simple and standardised approach to communication
		 you don't have to worry about how to format data, how to format request each time - its all standardised and industry use
- Scale-able and stateless
	- As service grows in complexity, you can easily make modifications
	- You don't have to worry about what data is in which state and keep track of that across client and server. 
- High performance because they support caching

CRUD operations:
- Like every letter has a stamp, every HTTP message, has a verb. if i want to load a website, i say "HTTP get some address". The response you get has code and data.
- What it stands for and the HTTP method/operation equivalent:
	- Create (Post)
	- Read (Get)
	- Update (Put)
	- Delete (Delete)

To summarise, you have two machines communicating. One is a client that sends requests using HTTP protocols (verb, address, and some extra info sometimes), the other is a server that has an API that allows the client to communicate with it easily through rules for how access is allowed and how clients should behave. If those rules aren't met, you can't communicate with it and you get errors.


# **Misc**:

HTTP Errors Cheat-sheet: https://developer.mozilla.org/en-US/docs/Web/HTTP/Status

**Example**:

HTTP/icecream.com/API/Flavours
API is the place (the folders basically)
flavours is the resource

Endpoint (location you go to - the thing that you get back)

JSON (javascript object notation) formatted data

Protocol (a set of rules / agreed on process - this is the way we're going to do things)
	HTTP/HTTPS protocol
	handshake vs fistbump - both of them are allowed but you cant combine them, you have to agree on what to use.

curl makes by default a http get request. curl will send you the data
