# networking-fundamentals

My networking fundamentals learning notes and cybersecurity foundation concepts

# Understanding the OSI Model as a Cybersecurity Beginner
When I first started learning networking fundamentals, the OSI model felt confusing and overly theoretical.

There were 7 different layers, each with separate responsibilities, protocols, and terminology. Initially, it felt like I was just memorizing definitions without understanding how everything connected together.

What helped me most was shifting from:
> “memorizing layers”

to:
> “understanding how data actually travels across a network.”

# The 7 Layers of the OSI Model

| Layer | Name | Main Responsibility |
|---|---|---|
| 7 | Application | User-facing network services |
| 6 | Presentation | Data formatting/encryption |
| 5 | Session | Session establishment/management |
| 4 | Transport | End-to-end communication (TCP/UDP) |
| 3 | Network | IP addressing and routing |
| 2 | Data Link | MAC addressing and Ethernet frames |
| 1 | Physical | Electrical/physical transmission |

---

# What Initially Confused Me

## 1. Difference Between IP Address and MAC Address

This was one of the biggest points of confusion.

At first, I could not understand:
- why both addresses exist
- when each one is used
- why routers care about IP while switches care about MAC

What finally clarified it for me was this:

> IP addresses are used for end-to-end logical communication.

> MAC addresses are used for local hop-to-hop delivery.

That single distinction made packet forwarding much easier to visualize.

---

## 2. What Routers Actually Do

Initially, I thought routers somehow “knew” the final destination device directly.

Later, I learned that routers:
1. Read the destination IP address
2. Check their routing table
3. Determine the next hop
4. Use ARP to resolve MAC addresses
5. Rebuild Ethernet frames for the next network segment

This also helped me understand why:
- IP addresses usually remain unchanged end-to-end
- MAC addresses change at every router hop

---

## 3. Understanding Packet Flow

Networking started becoming clearer once I visualized:

```text
Host A → Router → Router → Host B
```

At every router:
- Layer 2 frame is removed
- Router examines Layer 3 IP information
- New Layer 2 frame is created
- Packet moves toward the next hop

That practical flow helped the OSI model feel much less abstract.

---

# Key Takeaways

## What Helped Me Learn Faster

- Stop memorizing definitions blindly
- Focus on packet flow visualization
- Understand what changes at each hop
- Learn which layer is responsible for each behavior

---

# Important Realizations

## Layer 3 — Network Layer
- Handles IP addressing and routing
- Routers operate here

## Layer 2 — Data Link Layer
- Handles MAC addressing and Ethernet frames
- Switches primarily operate here

## Layer 4 — Transport Layer
- TCP/UDP
- Reliability and end-to-end communication

---

# Why This Matters for Cybersecurity

As someone learning web application pentesting, understanding networking fundamentals is extremely important.

These concepts help explain:
- how HTTP/HTTPS traffic travels
- how proxies like Burp Suite work
- where requests can be intercepted
- how communication happens between client and server

Right now, I am focusing on building strong foundations before moving deeper into:
- web application security
- HTTP/HTTPS
- traffic interception
- authentication/session concepts
- cloud security later on

---

# Final Thought

The OSI model became much easier once I stopped seeing it as a list of layers and started seeing it as a real packet journey across networks.

Still learning, but the concepts are becoming much clearer with practice and visualization.
