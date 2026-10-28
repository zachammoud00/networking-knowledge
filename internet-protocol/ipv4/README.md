# 🔢 Internet Protocol Version 4 (IPv4)

## 1. Fundamentals

- **What is IPv4?**

  Internet Protocol version 4 (IPv4) is a network-layer protocol used to identify an interface within a network and determine the source and destination of packets. IPv4 addresses are unique within their addressing scope, where public addresses are globally unique, while private addresses can be reused across different networks.

- **Why do we need IPv4?**

  We need IPv4 addressing because it allows devices to communicate in two ways:

  1. With devices on an external network.
  2. With devices within an internal network.

  One of IPv4 addressing's roles is to function as an identifier, allowing data to be transmitted to another device (interface). This works similarly to postal addressing, where an address identifies a destination within a country, city or suburb, allowing people to send mail through the postal system.

  The main constraint is that an address must be unique within its intended scope. For example, if two houses in the same suburb shared the same address, how would we know which house to deliver the mail to if all we had was the address?

  (This should be avoided when assigning IP addresses within the same scope.)

  If we assume that a typical address is written in the form:

  ```text
  <number> <street name> <city> <postcode>
  ```

  Then we have the two addresses:

  1. 42 Wallaby Way, Sydney, 2000
  2. 42 Wallaby Way, Perth, 6000

  If we only analyse the number and street name, these two addresses appear to be the same, but as we continue, they differ in the city and postcode values.

  This can be related back to IP addresses, where they can share the same values in some octets but differ in others. However, the addressing scope must always be taken into consideration.

- **How is an IPv4 address represented?**

  An IPv4 address is represented using 32 bits, which means that there are a total of \(2^{32} = 4,294,967,296\) possible addresses in IPv4.

  Although the IP address itself is represented using 32 bits, it is written in a special format using four octets in dotted-decimal notation:

  ```text
  X.X.X.X
  ```

  Each X is a number between 0 and 255, represented by eight bits. To a computer, the IP address is represented in binary.

  For example:

  ```text
  Binary:  11111111.11111111.11111111.11111111
  Decimal: 255.255.255.255
  ```

  This gives us the IPv4 limited broadcast address.

  This builds on the example given in the previous question, where we saw that each IP address assigned to an interface within the same addressing scope must be unique.

  If we have the two IP addresses:

  ```text
  Decimal: 192.168.10.1
  Binary:  11000000.10101000.00001010.00000001

  Decimal: 192.168.10.2
  Binary:  11000000.10101000.00001010.00000010
  ```

  As we can see, the addresses differ in the fourth octet, which means they have different values. These addresses can be valid on the same network, provided they are valid host addresses for that network and are not already assigned to other interfaces.

  It should be noted that the addressing scope must always be taken into consideration, meaning that addresses belonging to the same network should not share the same IP address.
    

## 2. Addressing
- What is classful addressing?
- What are the different IPv4 address classes?
- What is the difference between the network and host portions of an address?


## 3. Subnetting
- What is a subnet?
- Why do we need subnets?
- What is a subnet mask?
- How do we identify the network and broadcast addresses?
- How do we calculate the number of usable host addresses?
