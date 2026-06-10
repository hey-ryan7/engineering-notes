# Day 2 -- HTTP Headers & Cookies

## What is a Header
An HTTP header is a piece of metadata sent along with a request or response. Headers provide additional information that helps the client and server communicate correctly.

## Why Do We Need Headers?
Headers allow clients and servers to exchange extra information besides the main data. They can describe the content type, authentication information, cookies and other details about the request or response.

## Common HTTP Headers
### Content-Type
Specifies the type of content being sent
#### Example:
Content-Type: application/json
### Accept
Tells the server what type of content the client can understand.
#### Example:
Accept: application/json
### User-Agent
Provides information about the client application making request.
#### Example: 
User-Agent: Chrome
### Authorization
Contains credentials used to authenticate the client.
### Cookie
Used by the browser to send sotred cookie data back to the server.
### Set-Cookie
Used by the server to instruct the browser to store a cookie.
## What is Metadat?
Metadata is data about data. For example, the body of a request may contain the actual content, while headers contain information describing that conent.
## What is a Cookie?
A cookie is a small piece of data sotred by the browser. It helps the server recognize a user across multiple requests.
## Why Do Cookies Exist?
HTTP is stateless and does not remember previous requests. Cookies help maintain state between requests.
