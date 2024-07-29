We need to subnet the network address 210.100.56.0 to meet the following requirements:

- **Number of needed usable subnets:** 6
- **Number of needed usable hosts:** 30

**Address Class:**
- The IP address 210.100.56.0 is in Class C, as the first octet (210) falls between 192 and 223.

**Default Subnet Mask for Class B:**
- The default subnet mask for Class C is 255.255.255.0 or /24.

### Custom Subnet Mask Calculation

To meet the requirements, you need:

- **6 usable subnets**
- **30 usable hosts per subnet**

1. **Calculate Number of Subnets Required:**
	- You need 6 usable subnets.
	- The number of subnets is determined by the number of bits borrowed from the host portion for subnetting.

To find out how many bits you need to borrow, calculate 2n≥Number of Subnets Needed2^n \geq \text{Number of Subnets Needed}2n≥Number of Subnets Needed, where nnn is the number of bits borrowed.
- For 6 subnets, 23=82^3 = 823=8 subnets is enough (since 2^2 = 4 is not enough).
- Therefore, you need to borrow 3 bits for subnetting.

**Calculate Number of Hosts per Subnet:**

- We need at least 30 usable hosts per subnet.
- The number of host addresses per subnet is 2m2^m2m, where mmm is the number of bits for hosts.

To calculate the number of bits required for hosts:

- For 30 usable hosts, we need 25=322^5 = 3225=32 total addresses (since 2^4 = 16 is not enough).
- Therefore, 5 bits are needed for hosts, which gives 32 - 2 = 30 usable addresses (subtracting 2 for network and broadcast addresses).

**Determine the Custom Subnet Mask:**

- Starting with a /16 default mask, you are borrowing 3 bits for subnetting, so the new subnet mask is /16 + 3 = /19.
- This custom subnet mask in decimal is 255.255.224.0.