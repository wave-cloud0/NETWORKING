# Altschool-project-07

## Task:

- `193.16.20.35/29`

What is the Network IP, number of hosts, range of IP addresses and broadcast IP from this subnet?

## Instruction: 
- Submit all your answer as a markdown file in the folder for this exercise.



##  DELIVERABLES:

### Subnet Mask
- /29,  

Total Bits = 32  
On Bits = 29  
Off Bits = 29 - 32 = 3

This means the first full 3 octet and part of the 4th octet are ones. We have  

Base 2: 1111 1111. 1111 1111. 1111 1111. 1111 1000

Base 10: 255 . 255 . 255 . 248

SUBNET MASK: `255 . 255 . 255 . 248`   




### Wildcard
- To get the wildcard we subtract our subnet mask from 255 . 255 . 255 . 255
 
 255 . 255 . 255 . 255  
-255 . 255 . 255 . 248  
  0  .  0  .  0  .  7

Our Wildcard = `0 . 0 . 0 . 7`  




### Number of Total Hosts
- To obtain our total hosts we use, 2^# of off bits

We have, 2^3 = 2 x 2 x 2 = 8  

Our Number of Total Hosts = `8`   




### Number of Useable Hosts
- To gain our number of valid hosts, we use, total host minus 2

we have, 8 - 2 = 6  

 Our Number of Useable Hosts = `6`  




### IP Class
- IP Classes include 
a = 1 -126 , b = 128 - 191 , c = 192 - 223 , d = 224 - 239 (multicast - send data e.g streaming, to multiple recipients) , e = 240 - 255 (Experimental)

0 and 127 are N/A    

With reference to our subnet mask we know our class is a   

NETWORK . NETWORK . NETWORK . HOSTS  

Base 2: 1111 1111. 1111 1111. 1111 1111. 1111 1000  


![ip_class](</images/ip_class.png>)      


Therefore, our IP Class = `Class C`  




### Network IP Address
- To get network address, convert all parts of the IP Address after the visible line to ZEROS and convert to base 10

IP Address = 1100 0000. 0001 0000. 0001 0100. 0010 0 | 011 = 193 . 16 . 20 . 35

Converting to zeros  
0010 0 | 011 = 0010 0 | 000

Remove the visible line and convert to base 10   

0010 0000 = 32

Therefore, our Network IP Address is = `193 . 16 . 20 . 32`  




### Broadcast IP Address
- To get broadcast address, convert all parts of the IP Address  after the visible line to ONES and convert to base 10

IP Address = 1100 0000. 0001 0000. 0001 0100. 0010 0 | 011 = 193 . 16 . 20 . 35


Converting to ones  
0010 0 | 011 = 0010 0 | 111

Remove the visible line and convert to base 10   

0010 0111 = 39

Therefore, our Broadcast IP Address is = `193 . 16 . 20 . 39`  




### Range of IP Addresses
- To obtain our Range of IP Addresses, we use, 

Network IP Address +1, for the first ip address in the range   
Broadcast IP Address -1, for the last ip address in the range   

We have,   

193 . 16 . 20 . 32 + 1 = 193 . 16 . 20 . 33  
193 . 16 . 20 . 39 - 1 = 193 . 16 . 20 . 38

Therefore, our Range of IP Addresses is `193 . 16 . 20 . 33 -> 193 . 16 . 20 . 38`  




### VERIFICATION
- [VERIFY ANSWERS](https://www.calculator.net/ip-subnet-calculator.html)  
