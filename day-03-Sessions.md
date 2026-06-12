# Day 3 — Sessions

## What is a Session

A session is data created and stored by the server to keep track of a user across multiple requests. The server generates a unique Session ID and sends it to the browser, usually through a cookie. On future requests, the browser sends the Session ID back to the server, allowing the server to identify the user and retrieve their session data.

---

## Why Do We Need Sessions

HTTP is stateless, which means it does not remember previous requests. Without sessions, users would need to authenticate themselves on every request. Sessions solve this problem by allowing the server to recognize returning users and maintain state across multiple requests.

---

## What is a Session ID

A Session ID is a unique, long, and hard-to-guess identifier that represents a specific user session. It does not contain sensitive information such as passwords. The server uses the Session ID to find the corresponding session data and identify the user.

---

## Session vs Cookie

A cookie is a small piece of data stored in the browser and sent with future requests to the server.

A session is data stored on the server that contains information about a user's state.

In session-based authentication, the browser usually stores the Session ID inside a cookie, while the actual session data remains on the server.

---

## Login Flow

1. The user enters their email and password and submits the login form.
2. The browser sends an HTTP POST request to the server.
3. The server validates the credentials.
4. If the credentials are correct, the server creates a session and generates a Session ID.
5. The server sends a response containing a Set-Cookie header with the Session ID.
6. The browser stores the cookie.
7. On future requests, the browser automatically sends the cookie back to the server.
8. The server uses the Session ID to identify the user and return the requested data.
