# CSU33031-1

![Trinity College Dublin Logo]

## Coláiste na Tríonóide, Baile Átha Cliath
## Trinity College Dublin
Ollscoil Átha Cliath | The University of Dublin

---

### Faculty of Engineering, Mathematics & Science
### School of Computer Science and Statistics

---

**Integrated Computer Science Programme** — **Semester 1 Exam**

Senior Freshman  
BA (Mod) Business and Computing  
Junior Sophister  

---

## Computer Networks

**Date:** 09 DEC 2025 — **Time:** 09.30 – 12.30

**Prof. Stefan Weber**

---

### Instructions to Candidates:

- Answer **2 questions**.
- Both questions carry equal marks (**50 marks**).
- Answer each question in a **separate** answer book.
- If you think details such as values or labels are missing from questions, state this in your answer, make necessary assumptions and explain these assumptions briefly.

### Materials permitted for this examination:

- Calculator (non-programmable)

---

## Question 1

### a) Flow Control and ARQ Mechanisms [25 marks]

One of the tasks of the Link layer in the OSI stack is called "flow control". The High-Level Data Link Control (HDLC) protocol defines a number of types of frames shown in Figure 1.

Assume that node A, address `10110011`, uses HDLC to transmit 3600 bytes in 4 frames to node B, address `11101010`. The code in an S-Frame for an acknowledgement is `00` and for a negative acknowledgement is `11`. The flag byte consists of the bit-sequence `01111110`.

**i)** Draw the exchange of the frames in as much detail as possible for a **Go-Back-N** approach and for a **Selective-Repeat** approach. Assume that Frame 2 is corrupted during transmission. Your diagram should be accompanied by an explanation of the process and how each approach handles the error recovery differently.

**ii)** Explain the process of **bit stuffing** that takes place when the information being transferred includes the same bit-sequence as the flag byte. Demonstrate this process on the following data sequence: `011111101111110`.

**iii)** Discuss the relationship between the number of bits reserved for sequence numbers and the maximum window sizes for Go-Back-N and Selective Repeat. If 3 bits are used for sequence numbers, calculate the maximum sender window size for each approach and explain why they differ.

```
┌──────┬─────────┬─────────┬─────────────────┬─────┬──────┐
│ Flag │ Address │ Control │   Information   │ FCS │ Flag │  I-Frame
└──────┴─────────┴────┬────┴─────────────────┴─────┴──────┘
                      │
              ┌───┬───┼───┬───────┐
              │ 0 │   │P/F│       │
              └───┴───┴───┴───────┘
                N(S)       N(R)

┌──────┬─────────┬─────────┬─────┬──────┐
│ Flag │ Address │ Control │ FCS │ Flag │                    S-Frame
└──────┴─────────┴────┬────┴─────┴──────┘
                      │
              ┌───┬───┬───┬───────┐
              │ 1 │ 0 │P/F│       │
              └───┴───┴───┴───────┘
               Code        N(R)

┌──────┬─────────┬─────────┬───────────┬─────┬──────┐
│ Flag │ Address │ Control │ Mgmt.info │ FCS │ Flag │        U-Frame
└──────┴─────────┴────┬────┴───────────┴─────┴──────┘
                      │
              ┌───┬───┬───┬───────┐
              │ 1 │ 1 │P/F│       │
              └───┴───┴───┴───────┘
               Code    Code

              Figure 1: Types of HDLC frames
```

---

### b) Error Detection Mechanisms [25 marks]

A variety of mechanisms are used in telecommunication to provide error detection and correction.

**i)** Assume that a station intends to transmit the following bit sequence of 12 bits: `110101110011`. It will employ CRC as an error detection mechanism with the following polynomial: **x⁴ + x² + x + 1**. Explain and demonstrate the process that the station will follow to calculate the bit sequence to be transmitted. Show the process the receiver would employ to verify the integrity of the received data.

**ii)** Assume that a station intends to transmit the following 7-bit sequence: `1011010`. It will use Hamming Code as an error detection and correction mechanism. Explain and demonstrate the process that the station will follow to determine the bits to transmit, including the placement of parity bits. Show how the receiver would detect and correct a single-bit error if bit position 5 was flipped during transmission.

**iii)** Compare and contrast CRC, Hamming Code, and Internet Checksums. Discuss:
- Their computational complexity
- Their error detection capabilities
- Their suitability for different network layer protocols (Link layer vs. Network layer)
- Why Ethernet uses CRC while IPv4 uses checksums

---

**[Total 50 marks]**

---

## Question 2

### a) Medium Access Control Protocols [25 marks]

**i)** The Distributed Coordination Function (DCF) of IEEE 802.11 provides a mechanism for wireless stations to access the medium.

Assume that five stations S1 to S5 use 802.11 radios and are within each other's coverage area. Station S3 has just completed communicating with Station S1. Station S2 intends to transmit to station S4 and station S5 intends to transmit to station S1. The stations will use 802.11 DCF with RTS/CTS to get access to the medium.

Use diagrams to visualise the chronological exchange of the frames (including RTS, CTS, DATA, ACK) and the inter-frame spaces (DIFS, SIFS) that are involved in these exchanges. Explain how the backoff mechanism resolves contention between S2 and S5.

**ii)** Assume that instead of 802.11 DCF, four stations S1 to S4 use **Code-Division Multiple Access (CDMA)**. Station S1 intends to transmit the bit sequence `11` and Station S3 intends to transmit the bit sequence `00`; the other stations are silent. A '0' is encoded as -1, a '1' is encoded as +1, and silence is represented by 0.

The chip sequences of the stations are as follows:

| Station | Chip Sequence |
|---------|---------------|
| Station 1 | +1 -1 +1 -1 |
| Station 2 | +1 +1 -1 -1 |
| Station 3 | +1 -1 -1 +1 |
| Station 4 | +1 +1 +1 +1 |

Calculate the composite signal observed on the channel and demonstrate how Station S2 and Station S4 would decode the transmissions intended for them (if any). Verify the orthogonality property of the chip sequences.

**iii)** Compare CDMA with CSMA/CD in terms of:
- How collisions are handled
- Efficiency under light vs. heavy network load
- Suitability for wired vs. wireless networks

---

### b) Point Coordination Function and Polling [25 marks]

**i)** Assume that the communication scenario from part (a)(i) would use **802.11 PCF** instead of 802.11 DCF, and that an access point AP is present as the point coordinator. Describe the frames that will be exchanged by the stations and the inter-frame spaces involved. Include the Contention-Free Period (CFP) and Contention Period (CP) in your explanation. Use diagrams to visualise the chronological exchange.

**ii)** Discuss the advantages and disadvantages of PCF compared to DCF for:
- Real-time applications (e.g., VoIP, video streaming)
- Bursty data traffic (e.g., web browsing)
- Network scalability

**iii)** Explain why PCF has seen limited deployment in practice despite its theoretical advantages for Quality of Service (QoS), and briefly mention how later standards (802.11e) addressed medium access for QoS.

---

**[Total 50 marks]**

---

## Question 3

### a) Network Address Translation and Packet Routing [25 marks]

Assume that a node A intends to communicate with a node E over a number of intermediate nodes, B to D, as shown in Figure 2. The nodes use IEEE 802.3 Ethernet as the Link layer protocol for the connections between them, and node B acts as a **NAT gateway** for the local network that includes node A. Define IPv4 addresses, Ethernet addresses, and routing information as you see appropriate.

```
    ┌─────────────────┐                    ┌─────────────────┐
    │  192.168.1.0/24 │                    │  134.226.0.0/16 │
    │                 │                    │                 │
    │   ┌───┐  ┌───┐  │    ┌───┐  ┌───┐    │   ┌───┐  ┌───┐  │
    │   │ A │──│ B │──│────│ C │──│ D │────│───│   │──│ E │  │
    │   └───┘  └───┘  │    └───┘  └───┘    │   └───┘  └───┘  │
    │         NAT     │                    │                 │
    └─────────────────┘                    └─────────────────┘
         Private                                Public
         Network                               Network

        Figure 2: A Topology of two networks connected by routers
```

**i)** Describe the information that node B will keep in its **NAT translation table** in order to act as a NAT gateway. Explain how this information is used by B to process:
- Outgoing IPv4 packets from A destined for E
- Incoming IPv4 packets from E destined for A

Include an example of a NAT table entry showing the mapping between internal and external addresses/ports.

**ii)** Describe the IPv4 packet that A would issue (including source IP, destination IP, TTL, and relevant header fields) and trace the routing process of the IPv4 packet from A to E at each intermediate hop. Explain what changes are made to the packet at each router.

**iii)** Describe the Link layer frames encapsulating the IPv4 packet, assuming all links use Ethernet. Explain the **ARP (Address Resolution Protocol)** process used to resolve IPv4 addresses to Ethernet MAC addresses at each hop. Show the source and destination MAC addresses in the Ethernet frame at each segment of the journey.

---

### b) Routing Protocols [25 marks]

Distance Vector Routing and Link State Routing describe two fundamental types of routing protocols.

**i)** Give a description of both **Distance Vector Routing** (e.g., RIP) and **Link State Routing** (e.g., OSPF) in your own words. Compare the two approaches in terms of:
- Information shared between routers
- Convergence time
- Memory and bandwidth requirements
- Scalability

**ii)** Consider the network topology shown in Figure 3, representing a simplified campus network with 6 routers. Apply the **Distance Vector algorithm** to establish the routing table at router A. Show at least 3 iterations of the algorithm, demonstrating how routers exchange distance vectors and update their tables.

```
                    ┌───┐
                    │ A │
                   /     \
                  2       4
                 /         \
            ┌───┐           ┌───┐
            │ B │─────3─────│ C │
            └───┘           └───┘
              │               │
              1               2
              │               │
            ┌───┐           ┌───┐
            │ D │─────5─────│ E │
            └───┘           └───┘
                \         /
                 3       1
                  \     /
                   ┌───┐
                   │ F │
                   └───┘

    Figure 3: Campus network topology with link costs
```

**iii)** Explain the **"Count to Infinity"** problem using the topology in Figure 3. Assume that the link between A and B fails. Demonstrate how this problem manifests and discuss solutions such as:
- Split Horizon
- Poison Reverse
- Hold-down timers

---

**[Total 50 marks]**

---

## End of Examination

---

### Marking Scheme Summary

| Question | Part | Marks |
|----------|------|-------|
| 1 | (a) Flow Control & ARQ | 25 |
| 1 | (b) Error Detection | 25 |
| 2 | (a) MAC Protocols (DCF, CDMA) | 25 |
| 2 | (b) PCF and Polling | 25 |
| 3 | (a) NAT and Routing | 25 |
| 3 | (b) Routing Protocols | 25 |

**Total: 100 marks (Answer any 2 questions for 100 marks)**

---

*© Trinity College Dublin, The University of Dublin 2025*
