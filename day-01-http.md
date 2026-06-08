# Day 1 — HTTP Fundamentals

## What is HTTP
HTTP is a client-server protocol that forms the foundation of data transfer on the web. It can transfer different types of data such as text, HTML documents, images, and videos.

## Client and Server
The client initiates a request (usually a browser), and the server processes the request and returns a response based on it.

## Request and Response
A request is the data sent from the client to the server.
A response is the data sent from the server back to the client.

## What is a Resource
Anything that can be transferred over HTTP is called a resource.

## Being Stateless
HTTP is stateless, which means it does not remember previous requests.
However, sessions can be used on top of HTTP to maintain user state.

## Basic HTTP Flow
1. You enter a website URL in the browser  
2. DNS translates the domain into an IP address  
3. TCP establishes a connection  
4. (Optional) TLS encrypts the connection  
5. The browser sends an HTTP request  
6. The server processes the request  
7. The server sends back a response  
8. The browser renders the response
