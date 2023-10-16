# hands-on-tcp-udp-wireshark
Kelas Jarkom - D
Duevano Fairuz Pandya (5025211052)

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
Sequence number is 1068969752, Flag 0x012 identifies the segment as SYNACK, Acknowledgement number is 4236649188, Acknowledgement number is determined as the next value after the sequence number of the SYN segment (4236649187).

----------------------------------------------------------------------------------------------------------------------------------
# No. 5
### Soal
What is the sequence number of the TCP segment containing the header of the HTTP POST command? How many bytes of data are contained in the payload (data) field of this TCP segment? Did all of the data in the transferred file alice.txt fit into this single segment?

### Penyelesaian

----------------------------------------------------------------------------------------------------------------------------------
# No. 6
### Soal
Consider the TCP segment containing the HTTP “POST” as the first segment in the data transfer part of the TCP connection.

### Penyelesaian

----------------------------------------------------------------------------------------------------------------------------------
# No. 7
### Soal
What is the length (header plus payload) of each of the first four data-carrying TCP segments?

### Penyelesaian

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
# No. 1
### Soal
Select the first UDP segment in your trace. What is the packet number of this segment in the trace file?

### Penyelesaian

----------------------------------------------------------------------------------------------------------------------------------
# No. 2
### Soal
By consulting the displayed information in Wireshark’s packet content field for this packet (or by consulting the textbook), what is the length (in bytes) of each of the UDP header fields?

### Penyelesaian

----------------------------------------------------------------------------------------------------------------------------------
# No. 3
### Soal
The value in the Length field is the length of what?

### Penyelesaian

----------------------------------------------------------------------------------------------------------------------------------
# No. 4
### Soal
What is the maximum number of bytes that can be included in a UDP payload?

### Penyelesaian

----------------------------------------------------------------------------------------------------------------------------------
# No. 5
### Soal
What is the largest possible source port number?

### Penyelesaian

----------------------------------------------------------------------------------------------------------------------------------
# No. 6
### Soal
What is the protocol number for UDP?

### Penyelesaian

----------------------------------------------------------------------------------------------------------------------------------
# No. 7
### Soal
Examine the pair of UDP packets in which your host sends the first UDP packet and the second UDP packet is a reply to this first UDP packet.

### Penyelesaian

----------------------------------------------------------------------------------------------------------------------------------
