# Data Representation
---
*Date :*  24-10-2022 
*Module :* #CM10194 
*Teacher*: 
*Resources :*

---
##### Contents: 
> [[#Numeration Systems]]
> [[#Signed integers]]
> [[#Floating Point Binary]]
> 
--- 

Electronic computers are based on two-state devices(trasnsistors and logic gates). This can be related to the binary system. 

### Numeration Systems
All numeration systems are representational, i.e. a form of coding. 
Coding should be devised so that the system:
	•has few symbols that are easy to remember;
	•is unambiguous;
	•is economical in use (the higher the base more economical);
	•is a useful quantitative measure;
	•can be easily manipulated, e.g. to perform arithmetic.

Some examples of numerations systems: 
	Decimal notation: 10 symbols (0-9)
	Octal notation: 8 symbols (0-7)
	Binary notation: 2 symbols(0 and 1)

Examples: 
	Convert $134_8$ to decimal. 
		$1 \times 8^2 + 3 \times 8^1 + 4 \times 8^0 = 64 + 24 + 4 = 92$ 
	Convert $1101_2$ to decimal
		$1 \times 2^3 + 1 \times 2^2 + 0 \times 2^1 + 1 \times 2^0 = 8 + 4 + 0 + 1 = 13$ 
	Convert $1FCB_{16}$ to decimal
		$1 \times 163 + 15 \times 162 + 12 \times 161 + 11 \times 160 = 8139$ 

A binary digit(0 or 1) is called a bit.

Elements of the numeration system are that: 
- as many digit symbols as the base are needed;
- the decimal system’s base or radix of ten, the cardinal number of standards in the basic set, is denoted by ‘10’;
- place values increase from right to left in successive powers of the base (a positional system);
- addition is used to make up a number consisting of combinations of digits and multiplication is used to make up the number represented by a digit in a specific place;
- there is an agreed starting point (the ‘unit’ place); and
- a point is used to denote this place.

### Signed integers

###### Sign and Magnitude
- The first bit represent the sign of the integer (0 for positive, 1 for negative)
- The remaining n bits represent the magnitude 

|       **Advantages**           | **Disadvantages**                         |
| -------------------- | ------------------------------------- |
| Easy to read         | Two reprentations of zero             |
| Symmetric about zero | Only 255 values represented in a cell |
|                      | Arithmetic becomes                                       |

###### One's Complement
- Positive numbers are represent by adding a leading 0 as before. 
- Negative integers (-n) are represented by swapping 1's and 0's in n. 
![[Pasted image 20221025095259.png]]

This method simplifies arithmetic but leaves us with two representation of zero(+0, -0). 

###### Two's Complement 
We represent negative numbers(-n) by swapping 0's and 1's in n like with One's complement and then adding 1. 
We can represent numbers two's complement by follwing the steps:
	- First write the bit pattern for the positive number
	- Swap the numbers after the first 1

### Scientific Notation
This is where Mantissa and Exponent is used to represent floating point numbers. 
Scientific notation is useful because: 
	- It is simple to generate
	- Compact representation
	- Accurate
Disadvantages of scientific notation:
	- Some numbers can't be represented exactly e.x. $\frac{1}{3}, \pi$ 
	- Rounding erros

Any number can be represented in terms of two quantities:
	- Signed Mantissa (m)
	- Signed Exponent (x)
$Number =\pm m \times R \pm x$ where $R$ is the radix of the system. (10 in decimal)
The number is normalised if $1 \le  |m| < R$  (except zero)

### Floating Point Binary
$Number = \pm m \times 2^{\pm x}$
![[Pasted image 20221031114449.png | 300]]

![[Pasted image 20221101092345.png]]
>Learn converting numbers systems using the mantissa and the exponent. 

Normalised binary floating point number always has a 1 to the left of the binary point. 