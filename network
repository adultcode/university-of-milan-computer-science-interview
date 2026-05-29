# 🌐 Computer Networks — Expanded Crash Guide

> Use this as a quick review map before interviews.
> Try to explain each topic in **60–90 seconds**.

---

# 📚 Core Goal

* Understand how computers communicate
* Learn basic networking protocols
* Understand reliability and data transmission concepts
* Explain transport and application layer protocols

### Most Common Interview Questions

* TCP vs UDP
* ARQ
* Go-Back-N vs Selective Repeat
* IP
* DNS
* HTTP vs HTTPS
* Client-Server Model

---

# 📦 IP (Internet Protocol)

IP is the **network-layer protocol** responsible for:

* Addressing devices
* Routing packets across networks

IP moves packets from source to destination.

---

## Important Point

IP itself does **not guarantee**:

* Delivery
* Ordering
* Reliability

Higher-level protocols like TCP handle reliability.

---

## Example

When sending data:

1. Device creates packets
2. IP adds source & destination addresses
3. Routers forward packets through networks

## ✅ Interview Answer

> IP provides addressing and routing; reliability is usually handled by higher layers such as TCP.


---

# 🔒 TCP (Transmission Control Protocol)

TCP is:

* Connection-oriented
* Reliable
* Ordered

It ensures data arrives correctly and in order.

---

## TCP Features

| Feature            | Purpose                   |
| ------------------ | ------------------------- |
| Retransmission     | Resend lost packets       |
| Ordered Delivery   | Maintain correct order    |
| Flow Control       | Prevent receiver overload |
| Congestion Control | Reduce network congestion |

---

## Common Uses

* Web browsing
* File transfer
* Email
* Banking systems

---

## Trade-Off

Reliable but heavier than UDP.

## ✅ Interview Answer

> TCP is reliable and ordered, but it has more overhead than UDP.


---

# ⚡ UDP (User Datagram Protocol)

UDP is:

* Connectionless
* Lightweight
* Faster than TCP

It does **not guarantee**:

* Delivery
* Ordering
* Retransmission

---

## Common Uses

* Video streaming
* Voice calls
* Online games
* Live broadcasts

---

## Important Point

Applications handle reliability if needed.

## ✅ Interview Answer

> UDP is faster and simpler, but reliability must be handled by the application if needed.


---

# 🔄 ARQ (Automatic Repeat reQuest)

ARQ is a family of protocols for error control and reliability.

---

## How It Works

1. Sender sends packet
2. Receiver sends acknowledgment (ACK)
3. If packet lost/corrupted:

   * Sender retransmits

---

## Goal

Ensure reliable communication over unreliable networks.

## ✅ Interview Answer

> ARQ improves reliability by detecting missing/corrupted packets and retransmitting them.


---

# ↩️ Go-Back-N

Go-Back-N is an ARQ protocol using a sliding window.

---

## Key Idea

If one packet is lost:

* Sender retransmits:

  * Lost packet
  * All packets after it

---

## Advantages

* Simpler implementation

## Disadvantages

* Can resend many unnecessary packets

---

## Example

Packets:
`1 2 3 4 5`

If packet `3` is lost:

* Resend `3 4 5`

## ✅ Interview Answer

> Go-Back-N is simpler, but less efficient when only one packet is lost.


---

# 🎯 Selective Repeat

Selective Repeat improves efficiency.

---

## Key Idea

Only lost or corrupted packets are retransmitted.

---

## Advantages

* More efficient
* Less unnecessary retransmission

## Disadvantages

* More complex buffering
* More tracking logic

---

## Example

Packets:
`1 2 3 4 5`

If packet `3` is lost:

* Only resend `3`

## ✅ Interview Answer

> Selective Repeat is more efficient than Go-Back-N, but more complex.


---

# 📛 DNS (Domain Name System)

DNS translates human-readable domain names into IP addresses.

---

## Example

```text id="dns-example"
google.com → 142.250.x.x
```

Before connecting to a website:

1. Browser asks DNS server
2. DNS returns IP address
3. Connection starts

---

## Important Point

Humans remember names easier than numbers.

## ✅ Interview Answer

> DNS is like the phonebook of the Internet: it maps names to addresses.


---

# 🌍 HTTP & HTTPS

HTTP is an application-layer protocol used for web communication.

It follows a:

* Request → Response model

---

# HTTP

Not encrypted.

---

# HTTPS

HTTPS = HTTP + TLS encryption

Adds:

* Encryption
* Authentication
* Integrity protection

---

## Example

### HTTP Request

```text id="http-example"
GET /index.html HTTP/1.1
```

---

## Why HTTPS Matters

Protects:

* Passwords
* Credit card data
* Private communication

## ✅ Interview Answer

> HTTP defines request-response communication between clients and servers; HTTPS secures it.


---

# 🖥️ Client–Server Model

In the client-server model:

| Component | Role                                     |
| --------- | ---------------------------------------- |
| Client    | Sends requests                           |
| Server    | Processes requests and returns responses |

---

## Example

### Web Browser

* Browser → Client
* Web server → Server

---

## Workflow

1. Client sends request
2. Server processes it
3. Server returns response

## ✅ Interview Answer

> The client initiates communication; the server waits for requests and returns resources or results.


---

# ⚖️ TCP vs UDP Quick Comparison

| Feature     | TCP                 | UDP               |
| ----------- | ------------------- | ----------------- |
| Connection  | Connection-oriented | Connectionless    |
| Reliability | Reliable            | Unreliable        |
| Ordering    | Guaranteed          | Not guaranteed    |
| Speed       | Slower              | Faster            |
| Overhead    | Higher              | Lower             |
| Typical Use | Web, email, files   | Streaming, gaming |

---

# ⚡ Go-Back-N vs Selective Repeat

| Feature        | Go-Back-N                       | Selective Repeat  |
| -------------- | ------------------------------- | ----------------- |
| Retransmission | Lost packet + following packets | Only lost packets |
| Efficiency     | Lower                           | Higher            |
| Complexity     | Simpler                         | More complex      |

---

# 🎯 Final Interview Tips

* Always explain trade-offs
* Mention reliability when discussing TCP
* Mention speed when discussing UDP
* Use real-world examples like web browsing or gaming
* Clearly explain differences between protocols

---

# ⚡ Quick Revision Checklist

* [ ] IP
* [ ] TCP
* [ ] UDP
* [ ] ARQ
* [ ] Go-Back-N
* [ ] Selective Repeat
* [ ] DNS
* [ ] HTTP vs HTTPS
* [ ] Client-Server Model

---

Good luck with your interview 🚀
