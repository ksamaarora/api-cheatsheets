# API Styles 

- REST 
- GraphQL
- gRPC
- SOAP
- WebSockets

APIs can be designed and implemented using various styles, each with its own principles, protocols, and use cases. Here are some of the most common API styles:

<img width="636" height="480" alt="Screenshot 2025-11-24 at 4 58 27 PM" src="https://github.com/user-attachments/assets/708b0e36-922d-459a-a35c-03aedafb8e41" />

1. **REST (Representational State Transfer)**:
   - REST is an architectural style that uses standard HTTP methods (GET, POST, PUT, DELETE) for communication.
   - It is stateless, meaning each request from a client to a server must contain all the information needed to understand and process the request.
   - RESTful APIs typically use JSON or XML for data exchange and are resource-based, with each resource identified by a unique URL.
   - Example: GitHub API, Twitter API.
   - ```GET /users/{username}```
   - Format: JSON, XML, HTML, Plain Text

2. **GraphQL**:
   - GraphQL is a query language for APIs that allows clients to request only the data they need.
   - It provides a more flexible and efficient way to interact with APIs compared to REST, as clients can specify the structure of the response.
   - GraphQL APIs have a single endpoint and use a schema to define the types and relationships of data.
   - Example: GitHub GraphQL API, Shopify API.
   - ```query { user(username: "john") { name, email } }```
   - Format: JSON

3. **gRPC (gRPC Remote Procedure Calls)**:
   - gRPC is a high-performance, open-source framework developed by Google for remote procedure calls.
   - It uses Protocol Buffers (protobuf) for data serialization, which is more efficient than JSON or XML.
   - gRPC supports multiple programming languages and provides features like authentication, load balancing, and bidirectional streaming.
   - Example: Google Cloud APIs, Netflix API.
   - ```rpc GetUser (UserRequest) returns (UserResponse);```
   - Format: Protocol Buffers (binary format), JSON, XML, Thrift, FlatBuffers

4. **SOAP (Simple Object Access Protocol)**:
   - SOAP is a protocol for exchanging structured information in web services using XML.
   - It is highly extensible and supports various transport protocols, including HTTP, SMTP, and TCP.
   - SOAP APIs are known for their strict standards and built-in error handling, making them suitable for enterprise applications.
   - Example: PayPal API, Salesforce API.
   - ```<soap:Envelope>...</soap:Envelope>```
   - Format: XML only

5. **WebSockets**:
   - WebSockets is a protocol that enables full-duplex communication between a client and server over a single, long-lived connection.
   - It is ideal for real-time applications, such as chat applications, online gaming, and live data feeds.
   - WebSocket APIs allow for low-latency communication and can send messages in both directions.
   - Example: Slack API, Coinbase API.
   - ```ws://example.com/socket```
   - Format: JSON, XML, Plain Text, Binary
