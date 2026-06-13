# Day 5 — Access Token & Refresh Token

## Why JWT Alone Is Not Enough

A long-lived JWT can become a security risk if it is stolen. If an attacker gains access to a valid token that expires in several days or weeks, they can impersonate the user until the token expires. Revoking JWTs can also be more difficult than invalidating server-side sessions.

---

## What Is an Access Token

An Access Token is a short-lived token used to access protected resources. It is often implemented as a JWT and usually expires within a few minutes or hours.

Short expiration times reduce the impact of token theft because a stolen token becomes useless after a relatively short period.

---

## What Is a Refresh Token

A Refresh Token is a long-lived token used to obtain new Access Tokens without requiring the user to log in again.

Refresh Tokens usually have a much longer lifetime than Access Tokens, such as several days or weeks. In more secure systems, Refresh Token Rotation can be used, where a new Refresh Token is issued every time a new Access Token is generated.

---

## Why Do We Need Both

Access Tokens are intentionally short-lived for security reasons. However, requiring users to log in every few minutes would create a poor user experience.

Refresh Tokens solve this problem by allowing users to obtain new Access Tokens without entering their credentials again.

---

## Authentication Flow

1. The user enters their credentials and submits the login form.
2. The server validates the credentials.
3. If the credentials are correct, the server issues an Access Token and a Refresh Token.
4. The client stores the tokens. The Refresh Token is often stored in an HttpOnly cookie.
5. The client sends the Access Token with requests to protected resources.
6. The server validates the Access Token and processes the request.
7. If the Access Token expires, the client sends the Refresh Token to request a new Access Token.
8. The server validates the Refresh Token and issues a new Access Token.

---

## Token Expiration

Token expiration is the point at which a token is no longer considered valid by the server.

Expiration limits the amount of time a stolen token can be used.

---

## What Happens When the Access Token Expires

When an Access Token expires, the server typically responds with a `401 Unauthorized` status code.

The client can then use the Refresh Token to request a new Access Token. If the Refresh Token is valid, the user remains logged in without noticing the renewal process.

---

## Logout Flow

1. The user clicks the logout button.
2. The Access Token is removed from the client.
3. The Refresh Token is removed or invalidated.
4. The user is redirected to the login page.
5. Future requests require authentication again.

---

## Token Rotation

Token Rotation is a security technique where a new Refresh Token is issued whenever a new Access Token is generated.

This makes stolen Refresh Tokens easier to detect and limits the damage that can be caused if a token is compromised.

---

## Advantages

* Better security through short-lived Access Tokens
* Improved user experience through Refresh Tokens
* Reduced impact of token theft
* Works well in distributed systems and APIs

---

## Disadvantages

* More complex than using a single JWT
* Requires additional token management logic
* Refresh Token storage and rotation add implementation complexity
