Application Programming Interface

Software that sits on servers and orchestrates how info is processed and retrieved from the server.

Example:
Imagine if I was Facebook and I allowed the website to access any information it wanted, in any format it could from the Facebook Databases - it would be chaos. For this reason, Facebook built an API to control:

- Who can access the data
- How much data they can access
- How often they can retrieve data
- Whose data can be accessed

APIs are accessed via making HTTP requests to different URLs. For example, if I wanted to get information about a user on Github, I could make a request to the following URL:

https://api.github.com/users/USERNAME

I would use curl to do this: 
```curl https://api.github.com/users/USERNAME```


![[Pasted image 20250121072427.png]]

The Path/Resource (6) and Query Strings (7) are changed to access different parts of an API

# Rest API:

Representational
State
Transfer

Works kind of how a website does - you make a call from a client to a server, and you get data back over the HTTP protocol

**example:**

Facebook has an API called graph that you can use to get JSON formatted data organised in key:value pairs on any page you want by changing www.facebook.com/youtube to graph.facebook.com/youtube

now if you want to filter it, you can add ?fields=id,name,likes to the end like this:
graph.facebook.com/youtube?fields=id,name,likes