# **The Foundation of REST API: HTTP**

**What is HyperText?**

**HTTP (HyperText Transfer Protocol)** owes its name to **hypertext**.

So, what exactly is hypertext?

Imagine a blend of text, images, and videos that are stitched together by the magic of **hyperlinks**. These links serve as portals that allow us to jump from one set of hypertext to another. **HTML (HyperText Markup Language)** is a prime example of hypertext.

HTML is a plain text file. It’s packed with many tags that define links to images, videos, and more. After the browser interprets these tags, it transforms the seemingly ordinary text file into a webpage filled with text and images.

---

# **HTTP/1.1, HTTP/2, and HTTP/3**

HTTP 1 started in 1996 followed by HTTP 1.1 the very next year. In 2015, HTTP 2 came about and in 2019 we got HTTP 3.

<img width="1272" height="1035" alt="image" src="https://github.com/user-attachments/assets/a5d40365-dfe5-4f61-bae3-1efdabb06114" />

* **HTTP/1.0**, finalized and formally documented in 1996, had a key limitation: **each request required a separate TCP connection**.
  In simple words, if a webpage had 10 images, the browser had to open 10 separate connections to fetch those images, leading to delays.

* **HTTP/1.1**, introduced in 1997, brought significant improvements. It introduced **persistent connections**, allowing multiple requests and responses to be sent over a single TCP connection. This reduced latency and improved overall performance.
  It allowed TCP connections to remain open for multiple requests, reducing the overhead of establishing new connections.
  However, it still had limitations, such as **head-of-line blocking (HOL)**, where a delay in one request could block subsequent requests.

* **HTTP/2.0**, published in 2015, sought to tackle the HOL blocking issue. It implemented **request multiplexing**, a strategy to eliminate HOL blocking at the application layer.
  HTTP/2.0 introduced the concept of **HTTP streams**. Each stream is a bidirectional flow of data within a single TCP connection.
  This means that **multiple requests and responses can be sent simultaneously** over the same connection without waiting for one to finish before starting another.
  This significantly improved performance, especially for web pages with many resources.

* **HTTP/3**, the latest version, builds upon the advancements of HTTP/2.0 and introduces a new transport protocol called **QUIC (Quick UDP Internet Connections)**.
  QUIC uses **UDP instead of TCP**, enabling faster connection establishment and better handling of packet loss.
  QUIC streams share the same QUIC connection, requiring no additional handshakes or slow starts.
  QUIC streams are delivered **independently**, meaning packet loss in one stream does not impact others.
  In simple words, if you are streaming a video and downloading a file simultaneously, packet loss in the video stream won’t affect the file download stream.

---

# **What makes HTTP/2 faster than HTTP/1?**

The key features of HTTP/2 play a big role in this.

* **Binary Framing Layer**
  HTTP/2 encodes the messages into binary format. This allows the messages to be divided into smaller units called **frames**, which are then sent over the TCP connection, resulting in more efficient processing.

* **Multiplexing**
  The binary framing allows full request and response multiplexing. Clients and servers can interleave frames during transmission and reassemble them on the other side.

* **Stream Prioritization**
  With stream prioritization, developers can customize the relative weight of requests or streams to make the server send more frames for higher-priority requests.

* **Server Push**
  Since HTTP/2 allows multiple concurrent responses to a client’s request, a server can send additional resources along with the requested page to the client.

* **HPACK Header Compression**
  HTTP/2 uses a special compression algorithm called **HPACK** to make the headers smaller for multiple requests, thereby saving bandwidth.

---