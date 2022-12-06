# [UVa 845](https://onlinejudge.org/external/8/845.pdf) - Traffic Lights

Many gas stations use plastic digits on an illuminated sign to indicate prices. When there is an
insufficient quantity of a particular digit, the attendant may substitute another one upside down.
The digit “6” looks much like “9” upside down. The digits “0”, “1” and “8” look like themselves.
The digit “2” looks a bit like a “5” upside down (well, at least enough so that gas stations use it).
Due to rapidly increasing prices, a certain gas station has used all of its available digits to display the
current price. Fortunately, this shortage of digits need not prevent the attendant from raising prices.
She can simply rearrange the digits, possibly reversing some of them as described above.

![image](https://user-images.githubusercontent.com/54819920/205984446-38e16e20-5ce6-4f71-99f2-d3b6f01fac5b.png)

The input consists of several lines, each containing between 2 and 30
digits (to account for future prices) and a decimal point immediately before the last digit. There are
no useless leading zeroes; that is, there is a leading zero only if the price is less than 1. You are to
compute the next highest price that can be displayed using the same digits and the same format rules.
An input line containing a decimal point alone terminates the input. If the price cannot be raised, print
‘The price cannot be raised.’


The goal is to find the next price using only the digits currently displayed on the sign.
Definintion:
Next Price - the price that is higher than the first price, but lower than any other combination of prices.

```
Sample Input:
65.2
76.7
77.7
.
Sample Output:
65.5
77.6
The price cannot be raised.
```

uDebug:
```
Sample Input:
**15444.1**
0.9
0.1
0.2
0.3
0.6
**324317.3**
255555.5
**2692592.9**
0.0
0.1
1.1
5.5
6.6
**9.9**
6.9
.

Sample Output:
**211144.4**
6.0
1.0
0.5
3.0
0.9
**324331.7**
522222.2
**2692595.6**
The price cannot be raised.
1.0
The price cannot be raised.
The price cannot be raised.
6.9
**The price cannot be raised.**
9.6
