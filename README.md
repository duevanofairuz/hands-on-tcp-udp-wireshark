# hands-on-tcp-udp-wireshark
* Kelas Jarkom - D
* Duevano Fairuz Pandya (5025211052)

# TCP
# No. 1
### Soal
What is the IP address and TCP port number used by the client computer (source) 
that is transferring the alice.txt file to gaia.cs.umass.edu?

### Penyelesaian
![image](https://github.com/duevanofairuz/hands-on-tcp-udp-wireshark/assets/114162555/264ac781-5a4a-41a6-8b08-6a9ca21914f6)
![image](https://github.com/duevanofairuz/hands-on-tcp-udp-wireshark/assets/114162555/23d1d2d6-a482-4feb-9a93-822af938c885)
Source Address: 192.168.86.68
Source Port: 55639

----------------------------------------------------------------------------------------------------------------------------------
# No. 2
### Soal
What is the IP address of gaia.cs.umass.edu? On what port number is it sending 
and receiving TCP segments for this connection?

### Penyelesaian
![image](https://github.com/duevanofairuz/hands-on-tcp-udp-wireshark/assets/114162555/264ac781-5a4a-41a6-8b08-6a9ca21914f6)
![image](https://github.com/duevanofairuz/hands-on-tcp-udp-wireshark/assets/114162555/b55644f6-0b5f-494a-8c9a-2383213a13b0)
IP Address of gaia.cs.umass.edu: 128.119.245.12
Destination Port: 80

----------------------------------------------------------------------------------------------------------------------------------
# No. 3
### Soal
What is the sequence number of the TCP SYN segment that is used to initiate the TCP connection between the client computer and gaia.cs.umass.edu? What is it in this TCP segment that identifies the segment as a SYN segment? Will the TCP receiver in this session be able to use Selective Acknowledgments?

### Penyelesaian
![image](https://github.com/duevanofairuz/hands-on-tcp-udp-wireshark/assets/114162555/a5a68b24-fd79-4934-9966-7512f4fc7e77)
![image](https://github.com/duevanofairuz/hands-on-tcp-udp-wireshark/assets/114162555/e7f69db6-2e73-4a7a-9197-ead5abf5bcdf)

Sequence Number (raw): 4236649187
Flags: 0x002 (SYN)
SACK Permitted

----------------------------------------------------------------------------------------------------------------------------------
# No. 4
### Soal
What is the sequence number of the SYNACK segment sent by gaia.cs.umass.edu to the client computer in reply to the SYN? What is it in the segment that identifies the segment as a SYNACK segment? What is the value of theAcknowledgement field in the SYNACK segment? How did gaia.cs.umass.edu determine that value?

### Penyelesaian
![image](https://github.com/duevanofairuz/hands-on-tcp-udp-wireshark/assets/114162555/28c61c8a-4fd7-4dc5-a141-bd5dfcc26797)

Sequence Number: 0    (relative sequence number) & Sequence Number (raw): 1068969752, Flag 0x012 menandakan segmen SYNACK, Acknowledgment number (raw): 4236649188, Acknowledgement number didapatkan dari sequence number dari SYN segment ditambah 1 (ACK=Seq no+1).

----------------------------------------------------------------------------------------------------------------------------------
# No. 5
### Soal
What is the sequence number of the TCP segment containing the header of the HTTP POST command? How many bytes of data are contained in the payload (data) field of this TCP segment? Did all of the data in the transferred file alice.txt fit into this single segment?

### Penyelesaian
![image](https://github.com/duevanofairuz/hands-on-tcp-udp-wireshark/assets/114162555/0bd56a58-49ef-41a6-91ce-717161d2d59a)
Sequence Number: 152041  (relative sequence number) & Sequence Number (raw): 4236801228, TCP payload (1385 bytes), No

----------------------------------------------------------------------------------------------------------------------------------
# No. 6
### Soal
Consider the TCP segment containing the HTTP “POST” as the first segment in the data transfer part of the TCP connection.
![image](https://github.com/duevanofairuz/hands-on-tcp-udp-wireshark/assets/114162555/547ecbb3-f825-4948-8f6a-58f08f506df9)


### Penyelesaian
* At what time was the firstsegment(the onecontaining the HTTP POST) in the data-transfer part of the TCP connection sent?
[Time since reference or first frame: 0.024047000 seconds]

* At what timewas the ACK for this firstdata-containing segment received?
ACK frame 4 diterima diterima di frame 7 dengan clock time: [Time since reference or first frame: 0.052671000 seconds]

* What is the RTT for this first data-containing segment?
ada di frame 5 bagian SEQ/ACK analysis
[The RTT to ACK the segment was: 0.028624000 seconds]

* What is the RTT value the seconddata-carrying TCP segment and its ACK?
segement kedua yang dikirimkan ada di frame 5 lalu diterima di frame 8
[The RTT to ACK the segment was: 0.028628000 seconds]

----------------------------------------------------------------------------------------------------------------------------------
# No. 7
### Soal
What is the length (header plus payload) of each of the first four data-carrying TCP segments?

### Penyelesaian
![image](https://github.com/duevanofairuz/hands-on-tcp-udp-wireshark/assets/114162555/b6543a94-cdb8-44f8-99ce-b44613eb8e1a)

- frame: 4 : length = 32 + 1448 = 1480 bytes
- frame: 5 : length = 32 + 1448 = 1480 bytes
- frame: 6 : length = 32 + 1448 = 1480 bytes
- frame: 9 : length = 32 + 1448 = 1480 bytes
Sehingga total length dari 4 segment pertama adalah 1480 * 4 = 5920 bytes

----------------------------------------------------------------------------------------------------------------------------------
# No. 8
### Soal
What is the minimum amount of available buffer space advertised to the client by gaia.cs.umass.edu among these first four data-carrying TCP segments? Does the lack of receiver buffer space ever throttle the sender for these first four data carrying segments?

### Penyelesaian

----------------------------------------------------------------------------------------------------------------------------------
# No. 9
### Soal
Are there any retransmitted segments in the trace file? What did you check for (in the trace) in order to answer this question?

### Penyelesaian

----------------------------------------------------------------------------------------------------------------------------------
# No. 10
### Soal
How much data does the receiver typically acknowledge in an ACK among the first ten data-carrying segments sent from the client to gaia.cs.umass.edu? Can you identify cases where the receiver is ACKing every other received segment (see Table 3.2 in the text) among these first ten data-carrying segments?

### Penyelesaian

----------------------------------------------------------------------------------------------------------------------------------
# No. 11
### Soal
What is the throughput (bytes transferred per unit time) for the TCP connection?

### Penyelesaian

----------------------------------------------------------------------------------------------------------------------------------
# No. 12
### Soal
Use the Time-Sequence-Graph(Stevens) plotting tool to view the sequence number versus time plot of segments being sent from the client to the gaia.cs.umass.edu server.

### Penyelesaian

----------------------------------------------------------------------------------------------------------------------------------
# No. 13
### Soal
These “fleets” of segments appear to have some periodicity. What can you say about the period?

### Penyelesaian

----------------------------------------------------------------------------------------------------------------------------------

# UDP
![image](https://github.com/duevanofairuz/hands-on-tcp-udp-wireshark/assets/114162555/32ef2cf1-d20b-4c42-a505-c3a78fda6825)

# No. 1
### Soal
* Select the first UDP segment in your trace. What is the packet number of this segment in the trace file?
* What type of application-layer payload or protocol message is being carried in this UDP segment?
* Look at the details of this packet in Wireshark. How many fields there are in the UDP header? Look at the details of this packet in Wireshark. How many fields there are in the UDP header?

### Penyelesaian
Paket 5, SSDP, 4 Field (source port, destination port, length, checksum)

----------------------------------------------------------------------------------------------------------------------------------
# No. 2
### Soal
By consulting the displayed information in Wireshark’s packet content field for this packet (or by consulting the textbook), what is the length (in bytes) of each of the UDP header fields?

### Penyelesaian
Masing-masing field adalah 16 bit atau 2 byte, karena ada 4 field maka length masing-masing header dari UDP adalah `8 byte`

----------------------------------------------------------------------------------------------------------------------------------
# No. 3
### Soal
The value in the Length field is the length of what?

### Penyelesaian
Length dari paket UDP: payload 275 byte, header 8 byte

----------------------------------------------------------------------------------------------------------------------------------
# No. 4
### Soal
What is the maximum number of bytes that can be included in a UDP payload?

### Penyelesaian
Karena length adalah 16 bait field, maximum value nya adalah 65.535, dan headernya 8 byte, maka maximum payload nya adalah 65.527 byte

----------------------------------------------------------------------------------------------------------------------------------
# No. 5
### Soal
What is the largest possible source port number?

### Penyelesaian
65.535

----------------------------------------------------------------------------------------------------------------------------------
# No. 6
### Soal
What is the protocol number for UDP?

### Penyelesaian
![image](https://github.com/duevanofairuz/hands-on-tcp-udp-wireshark/assets/114162555/c9a87d06-679f-4a04-a65b-663135fb9c93)

Protocol: UDP (17)

----------------------------------------------------------------------------------------------------------------------------------
# No. 7
### Soal
Examine the pair of UDP packets in which your host sends the first UDP packet and the second UDP packet is a reply to this first UDP packet.
* What is the packet number of the first of these two UDP segments in the trace file?
* What is the packet number of the second of these two UDP segments in the trace file?
* Describe the relationship between the port numbers in the two packets.

### Penyelesaian
Paket 15, Paket 17, source port dari paket 15 (request) adalah destinasi port untuk paket 17 (reply) dan sebaliknya

----------------------------------------------------------------------------------------------------------------------------------
