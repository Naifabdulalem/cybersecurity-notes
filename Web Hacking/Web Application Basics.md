# Web Application Basics

> **Platform:** TryHackMe  
> **Difficulty:** Easy  
> **Status:** ✅ Completed  
> **Topics:** HTTP, URLs, Requests, Responses, Headers, Status Codes

## Introduction

In this room, I learned the basic concepts of how web applications communicate over the internet. Understanding HTTP requests, responses, URLs, and headers is essential before learning web application security.

## Web Application Overview

A web application is software that runs on a web server and is accessed through a browser. When I visit a website, my browser sends an HTTP request to the server, and the server responds with the requested content.

Basic workflow:

```text
Browser → HTTP Request → Web Server
Browser ← HTTP Response ← Web Server
```

## Uniform Resource Locator (URL)

A URL (Uniform Resource Locator) is the address of a resource on the internet.

Example:

```text
https://example.com/login
```

A URL usually contains:

- **Protocol** (https://)
- **Domain** (example.com)
- **Path** (/login)
- **Query Parameters** (optional)

Example with query parameters:

```text
https://example.com/search?q=burp
```

## HTTP Messages

HTTP communication consists of two messages:

- **Request** – Sent from the client (browser) to the server.
- **Response** – Sent from the server back to the client.

## HTTP Request

An HTTP request contains:

- Request method
- URL
- Headers
- Body (optional)

### Common HTTP Methods

| Method | Purpose |
|--------|---------|
| GET | Retrieve data |
| POST | Send data |
| PUT | Update existing data |
| DELETE | Remove data |

## HTTP Headers

Headers provide additional information about the request.

Some common headers include:

- Host
- User-Agent
- Cookie
- Content-Type
- Authorization

## HTTP Body

The body contains the actual data sent to the server. It is commonly used with methods like **POST** and **PUT**.

## HTTP Response

An HTTP response contains:

- Status line
- Headers
- Response body

The response body usually contains HTML, JSON, images, or other data requested by the client.

## Common HTTP Status Codes

| Code | Meaning |
|------|---------|
| 200 | OK |
| 301 | Moved Permanently |
| 302 | Found (Redirect) |
| 400 | Bad Request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal Server Error |

## Security Headers

Security headers help protect web applications from common attacks.

Some important security headers include:

- Content-Security-Policy (CSP)
- Strict-Transport-Security (HSTS)
- X-Frame-Options
- X-Content-Type-Options

## Practical Task

During the practical exercise, I created HTTP requests and observed the server's responses. This helped me understand how browsers communicate with web servers and how different request methods and headers affect the response.

## Key Takeaways

- Web applications communicate using HTTP.
- Every interaction between a browser and a server involves a request and a response.
- URLs identify resources on a web server.
- HTTP methods define the action performed on a resource.
- Headers provide additional information about requests and responses.
- Status codes indicate whether a request was successful or failed.
- Security headers improve the security of web applications.

## References

- TryHackMe – Web Application Basics
- Mozilla Developer Network (MDN): https://developer.mozilla.org/en-US/docs/Web/HTTP
