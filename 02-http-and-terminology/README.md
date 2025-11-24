# **HTTP and Terminology**

To effectvely work with APIs, it's essential to understand the underlying protocols and terminology. The most commonly used protocol for APIs is **HTTP (Hypertext Transfer Protocol)**, which is the foundation of data communication on the web.

Refer to this -> **[The Foundation of REST ApI: HTTP](/blogs/FoundationofRESTAPI-HTTP.md)**

* What is HyperText?
* HTTP/1.1, HTTP/2, and HTTP/3
* What makes HTTP/2 faster than HTTP/1?

---

> ### What is REST? How is it different from HTTP?

REST and HTTP are related but distinct concepts in web development.

**HTTP (Hypertext Transfer Protocol)** is a communication protocol that defines how messages are formatted and transmitted between clients (e.g., web browsers) and servers. It forms the foundation of data communication on the World Wide Web. HTTP defines methods like **GET**, **POST**, **PUT**, **DELETE**, etc., for performing various actions.

**REST (Representational State Transfer)** is an architectural style for building distributed systems, particularly web services. It's a set of constraints and principles that, when applied, result in a system that is scalable, performant, and maintainable.

Key REST principles include:

* **Client-Server**: Separation of concerns between the client and server.
* **Stateless**: Each request from a client to a server must contain all the information needed to understand the request. The server does not store any client context between requests.
* **Cacheable**: Responses from the server can be explicitly or implicitly marked as cacheable to improve performance.
* **Uniform Interface**: A standardized way for clients to interact with resources, typically using standard HTTP methods and resource-based URLs.
* **Layered System**: Architectural layers (e.g., proxies, load balancers) can be introduced without affecting the client or server.

RESTful APIs typically use HTTP as their underlying transport protocol. This means they leverage HTTP methods, status codes, and other features to implement the REST architectural style. However, **not all APIs that use HTTP are considered RESTful**. An API is only RESTful if it adheres to the specific constraints and principles of REST.

---

> # **API Terminology:**

1. **HTTP Versions**: Different versions of the HTTP protocol (e.g., HTTP/1.1, HTTP/2, HTTP/3) with varying features and performance characteristics.
   When we write HTTP, we usually refer to **HTTP/1.1** unless specified otherwise.

---

2. **HTTP Methods**: Standardized actions that can be performed on resources, such as **GET** (retrieve data), **POST** (create data), **PUT** (update data), **DELETE** (remove data), etc.

* **HTTP GET**: Used to retrieve data from a server. It does not change the state of the server and is considered a safe and **idempotent** method, meaning even if it is called multiple times, the result will be the same.

* **HTTP POST**: Used to send data to a server to create a new resource. It can change the state of the server and is **not idempotent**, meaning multiple identical POST requests may result in multiple resources being created.

* **HTTP PUT**: Used to update an existing resource or create a new resource if it doesn't exist. It is **idempotent**.

* **HTTP DELETE**: Used to remove a resource from the server. It is **idempotent**.

* **HTTP PATCH**: Used to apply partial modifications to a resource. It is **not necessarily idempotent**.

(Idemopotent means that making the same request multiple times will have the same effect as making it once. For example, calling DELETE on a resource multiple times will result in the same state as calling it once.)

---

3. **Status Codes**: Numeric codes returned by the server to indicate the outcome of an HTTP request (e.g., **200 OK**, **404 Not Found**, **500 Internal Server Error**).

HTTP Status Codes are grouped into five categories based on the first digit of the code:
![HTTP STatus Codes](/assets/HTTPStatusCodes.png)

* **1xx (Informational)**: Request received, continuing process.
* **2xx (Successful)**: The request was successfully received, understood, and accepted. Examples: **200 OK**, **201 Created**.
* **3xx (Redirection)**: Further action needs to be taken to complete the request. Examples: **301 Moved Permanently**, **302 Found**.
* **4xx (Client Error)**: The request contains bad syntax or cannot be fulfilled. Examples: **400 Bad Request**, **401 Unauthorized**, **404 Not Found**.
* **5xx (Server Error)**: The server failed to fulfill a valid request. Examples: **500 Internal Server Error**, **503 Service Unavailable**.

---

4. **Headers**: Metadata sent with HTTP requests and responses, providing additional information about the request or response (e.g., **Content-Type**, **Authorization**, **User-Agent**).

Whats inside the HTTP Headers?

HTTP requests are like asking for something from a server, and HTTP responses are the server’s replies. It’s like sending a message and receiving a reply.

An **HTTP request header** is an extra piece of information you include when making a request, such as what kind of data you are sending or who you are. In **response headers**, the server provides information about the response it is sending you, such as what type of data you’re receiving or if you have special instructions.

![HTTP Headers](/assets/WhatsInsideHTTPHeader.png)

---

5. **Payload/Body**: The data sent in the body of an HTTP request or response, often in formats like **JSON** or **XML**.

6. **Endpoints**: Specific URLs that represent resources or actions in an API. Example endpoint: `https://api.example.com/users`.

7. **Resources**: The data entities that an API exposes, such as users, products, or orders.

8. **CRUD Operations**: The basic operations that can be performed on resources: **Create**, **Read**, **Update**, **Delete**.

9. **Authentication**: The process of verifying the identity of a user or application accessing the API, often using methods like **API keys**, **OAuth**, or **JWT**. Refer to part 4 for more details.

10. **Rate Limiting**: A mechanism to control the number of requests a client can make to an API within a specified time frame, preventing abuse and ensuring fair usage.

11. **Caching**: The process of storing copies of responses to reduce server load and improve performance for subsequent requests.

12. **Throttling**: The process of limiting the number of requests a client can make to an API in order to prevent overloading the server.

13. **Versioning**: The practice of managing changes to an API by creating different versions (e.g., **v1**, **v2**) to ensure backward compatibility.

14. **Pagination**: A technique used to divide large sets of data into smaller, manageable chunks or pages, often implemented using query parameters like `limit` and `offset`.

---