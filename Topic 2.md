## ASCII table
- Stores only 128 characters
- Mostly english characters
- Unicode was made to replace characters that were not in ASCII, such as European, Cyrillic, Chinese Mandarin characters.
- Doing this allows people of different languages to use the computer.

## Decimal
Humans in their day to day life, use denary (or decimal) number system. (0 to 9)

## Binary
Binary Strings contains 1s and 0s. There are 2 categories of binaries:
- Signed
- Unsigned

Unsigned numbers are used for memory addresses, cluster numbers (in filesystems) and process identifiers (PID).<br><br>
If there are N bits in a binary number, the range of the numerical value will be: $$2^N -1$$

## Number Representation
Hexa decimal is base 16, (0 to 9 and A to F). Sometimes and 0x is added in front to represent things like memory addresses.

## Signed numbers
To represent the value type, the leftmost bit is used to represent positives or negatives. 0 would represent positive and 1 will represent negative.<br><br>
There are three ways to represent signed numbers:
| Sign and magnitude | 1's complement | 2's complement |
|---|---|---|

## example of system:
![example list](https://github.com/pendragons-code/FOC-in-depth/blob/master/assets/signed%20numbers.png)

## general formula
- <b>sign and magnitude</b>: negative values are representde by changing the most significant bit.
- <b>1's complement</b>: negative values are obtained by complementing each bit of the corresponding positive number.
- <b>2's complement</b> complement the bits and add 1

## example of conversion
Suppose a binary value: 0101 (+5)<br><br>
To form -5:
```
0101
to
1010 (1's complement)

+1 for 2's complement
1011
```

## 2's complement
2's complement is the most efficient way to carry out addition and subtraction operations.
![Complements](https://github.com/pendragons-code/FOC-in-depth/blob/master/assets/complements.png)

## Addition rules:
0+0 = 0<br>
1 + 0 = 1<br>
1 + 1 = 10<br>
1 + 1 + 1 = 11

## Subtraction rules
Form the 2’s-complement of the subtrahend (the bottom value) and then perform normal addition. This operation is done in exactly the same manner for both positive and negative numbers:
```
  1110 (-2)
- 1011 (-5)
-------------
    0011 (+3)
------------- 
```

## Overflow
Overflow occurs when the answer does not fit in the number range:

The range of expression is: $$-2^{n-1} to +2^{n-1}-1$$

## Sign exetension:
replicate the left hand most sign to extend it:
```
4 bits: 1011
8 bits: 1111 1011
```