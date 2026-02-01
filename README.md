# Jedha - Network Security Lab: Subnetting Assignment
**Student:** Pereyra
**Course:** Jedha Cybersecurity

## Part 1: IPv4 Calculations

### Exercise 1 - Equal Segmenting
Original Network: 192.168.10.0/24
Dividing into 4 subnets (2 bits borrowed -> /26 mask).
New Subnet Mask: 255.255.255.192

* Subnet 1: 192.168.10.0/26
  - Range: 192.168.10.1 to 192.168.10.62
  - Broadcast: 192.168.10.63
* Subnet 2: 192.168.10.64/26
  - Range: 192.168.10.65 to 192.168.10.126
  - Broadcast: 192.168.10.127
* Subnet 3: 192.168.10.128/26
  - Range: 192.168.10.129 to 192.168.10.190
  - Broadcast: 192.168.10.191
* Subnet 4: 192.168.10.192/26
  - Range: 192.168.10.193 to 192.168.10.254
  - Broadcast: 192.168.10.255

---

### Exercise 2 - VLSM Optimization
Starting from 192.168.10.0/24. 
Prioritizing departments by size to avoid address overlapping.

1. IT (50 devs): Needs /26 (64 addresses)
   - Network: 192.168.10.0/26
   - Range: 192.168.10.1 - 192.168.10.62
2. HR (25 devs): Needs /27 (32 addresses)
   - Network: 192.168.10.64/27
   - Range: 192.168.10.65 - 192.168.10.94
3. Sales (10 devs): Needs /28 (16 addresses)
   - Network: 192.168.10.96/28
   - Range: 192.168.10.97 - 192.168.10.110
4. Logistics (5 devs): Needs /29 (8 addresses)
   - Network: 192.168.10.112/29
   - Range: 192.168.10.113 - 192.168.10.118

---

## Part 2: IPv6 Subnetting

### Exercise 3 - /56 Subnets
Prefix: 2001:db8:abcd::/48
Incrementing the 4th hextet:
- Subnet 1: 2001:db8:abcd:0000::/56
- Subnet 2: 2001:db8:abcd:0100::/56
- Subnet 3: 2001:db8:abcd:0200::/56
- Subnet 4: 2001:db8:abcd:0300::/56

### Exercise 4 - /64 Subnets from 2001:db8:abcd:1000::/56
Breaking down the /56 block into 8 segments:
1. 2001:db8:abcd:1000::/64
2. 2001:db8:abcd:1001::/64
3. 2001:db8:abcd:1002::/64
4. 2001:db8:abcd:1003::/64
5. 2001:db8:abcd:1004::/64
6. 2001:db8:abcd:1005::/64
7. 2001:db8:abcd:1006::/64
8. 2001:db8:abcd:1007::/64
