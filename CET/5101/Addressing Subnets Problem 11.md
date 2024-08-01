### 1. Address Class:

The network address is 101.0.0.0. This address belongs to Class A (since the first octet, 101, falls within the range 1-126).

### 2. Default Subnet Mask:

The default subnet mask for a Class A address is: 255.0.0.0255.0.0.0255.0.0.0

### 3. Custom Subnet Mask:

We need to determine the custom subnet mask that will provide at least 250 usable subnets.

The formula for calculating the number of subnets is: 2n2^n2n where nnn is the number of bits borrowed.

To find the smallest nnn such that 2n≥2502^n \geq 2502n≥250: 28=2562^8 = 25628=256

So, n=8n = 8n=8 bits borrowed.

The default subnet mask for Class A is /8. By borrowing 8 bits, we get: 8+8=168 + 8 = 168+8=16

So, the custom subnet mask is: 255.255.0.0255.255.0.0255.255.0.0 (/16 subnet mask)

### 4. Number of Subnets:

We borrowed 8 bits from the original host part, providing: 28=2562^8 = 25628=256

### 5. Number of Usable Subnets:

In many systems, all subnets are usable, so we have 256 usable subnets.

### 6. Total Number of Host Addresses per Subnet:

With a /16 subnet mask, there are 2162^{16}216 addresses per subnet. 216=655362^{16} = 65536216=65536

### 7. Number of Usable Addresses per Subnet:

Subtracting 2 for network and broadcast addresses: 65536−2=6553465536 - 2 = 6553465536−2=65534

### 8. Number of Bits Borrowed:

We borrowed 8 bits (from /8 to /16).

### 9. Subnet Ranges:

Let's calculate the subnet ranges for the first 10 subnets.

|Subnet #|Network Address|First Usable Address|Last Usable Address|Broadcast Address|
|---|---|---|---|---|
|1|101.0.0.0|101.0.0.1|101.0.255.254|101.0.255.255|
|2|101.1.0.0|101.1.0.1|101.1.255.254|101.1.255.255|
|3|101.2.0.0|101.2.0.1|101.2.255.254|101.2.255.255|
|4|101.3.0.0|101.3.0.1|101.3.255.254|101.3.255.255|
|5|101.4.0.0|101.4.0.1|101.4.255.254|101.4.255.255|
|6|101.5.0.0|101.5.0.1|101.5.255.254|101.5.255.255|
|7|101.6.0.0|101.6.0.1|101.6.255.254|101.6.255.255|
|8|101.7.0.0|101.7.0.1|101.7.255.254|101.7.255.255|
|9|101.8.0.0|101.8.0.1|101.8.255.254|101.8.255.255|
|10|101.9.0.0|101.9.0.1|101.9.255.254|101.9.255.255|

### Summary:

- **Network Address Class:** A
- **Default Subnet Mask:** 255.0.0.0
- **Custom Subnet Mask:** 255.255.0.0 (/16)
- **Total Number of Subnets:** 256
- **Number of Usable Subnets:** 256
- **Total Number of Host Addresses per Subnet:** 65536
- **Number of Usable Addresses per Subnet:** 65534
- **Number of Bits Borrowed:** 8

### Table of First 10 Subnets:

| Subnet # | Network Address | First Usable Address | Last Usable Address | Broadcast Address |
| -------- | --------------- | -------------------- | ------------------- | ----------------- |
| 1        | 101.0.0.0       | 101.0.0.1            | 101.0.255.254       | 101.0.255.255     |
| 2        | 101.1.0.0       | 101.1.0.1            | 101.1.255.254       | 101.1.255.255     |
| 3        | 101.2.0.0       | 101.2.0.1            | 101.2.255.254       | 101.2.255.255     |
| 4        | 101.3.0.0       | 101.3.0.1            | 101.3.255.254       | 101.3.255.255     |
| 5        | 101.4.0.0       | 101.4.0.1            | 101.4.255.254       | 101.4.255.255     |
| 6        | 101.5.0.0       | 101.5.0.1            | 101.5.255.254       | 101.5.255.255     |
| 7        | 101.6.0.0       | 101.6.0.1            | 101.6.255.254       | 101.6.255.255     |
| 8        | 101.7.0.0       | 101.7.0.1            | 101.7.255.254       | 101.7.255.255     |
| 9        | 101.8.0.0       | 101.8.0.1            | 101.8.255.254       | 101.8.255.255     |
| 10       | 101.9.0.0       | 101.9.0.1            | 101.9.255.254       | 101.9.255.255     |