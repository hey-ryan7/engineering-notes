# Engineering Notes

My software engineering learning journey.

## Goals

* Learn deeply
* Build consistently
* Improve every day
* Understand how the web works under the hood
* Become a product-minded software engineer
* Complete projects instead of abandoning them
* Improve technical English
* Build a public portfolio of knowledge and projects

## Progress

### Day 1 — HTTP Fundamentals

Topics covered:

* What HTTP is
* Client-server architecture
* Requests and responses
* Resources
* Stateless communication
* Basic HTTP flow
* DNS
* TCP
* TLS

Key takeaway:

> HTTP is a stateless client-server protocol that forms the foundation of communication on the web.

---

### Day 2 — Headers & Cookies

Topics covered:

* HTTP headers
* Metadata
* Content-Type
* Accept
* User-Agent
* Authorization
* Cookie
* Set-Cookie

Learned:

* Why headers exist
* How browsers store cookies
* How cookies are sent back to servers
* How cookies help maintain user identity

Key takeaway:

> Cookies help browsers and servers maintain state across multiple HTTP requests.

---

### Day 3 — Sessions

Topics covered:

* Sessions
* Session IDs
* Session-based authentication
* Login flow
* Session vs Cookie

Learned:

* Sessions are stored on the server
* Browsers usually store only the Session ID
* Session IDs help servers recognize returning users
* HTTP remains stateless while sessions provide user state

Key takeaway:

> Session data lives on the server, while the Session ID is typically stored in a cookie.

---

### Day 4 — JWT (JSON Web Token)

Topics covered:

* Why JWT exists
* Stateless authentication
* JWT structure
* Header
* Payload
* Signature
* JWT authentication flow
* JWT vs Session

Learned:

* JWT stores claims inside the token
* The signature protects the token from tampering
* JWT reduces the need for server-side session storage
* JWT is commonly used in modern APIs and distributed systems

Key takeaway:

> Session-based authentication stores state on the server, while JWT-based authentication stores information inside the token.

---

## Current Learning Path

```text
HTTP
↓
Headers & Cookies
↓
Sessions
↓
JWT
↓
Access Token & Refresh Token
↓
OAuth
↓
Authentication Architecture
```

## Current Project

### identity-flow

A hands-on authentication project built to understand:

* Authentication
* Cookies
* Sessions
* JWT
* Access Tokens
* Refresh Tokens
* Protected Routes

Tech Stack:

* Next.js
* TypeScript
* PostgreSQL
* Prisma
* Tailwind CSS

Status:

🚧 In Progress
