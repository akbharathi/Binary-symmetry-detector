<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works
Working Principle

1) Inputs:

* 8 toggle switches (IN0–IN7) represent the binary input.

* A clock (CLK) and reset (RST_N) are available but not used in this pure gate design.

2) Pairwise Comparison:

* Each pair of bits (Di, Dj) from opposite ends is compared.

* This is done using an XNOR gate (equivalence gate).

* Example: D7 XNOR D0 = 1 if they are equal.

3) All Pairs Must Match:

* The results of all four XNOR comparisons are combined using AND gates.

* If every comparison outputs 1, the final AND gate outputs 1.

4) Output: 

* The final result drives an LED.

* LED ON → input word is symmetric.

* LED OFF → input word is not symmetric.

## How to test

1) Set Inputs

* Use switches IN0–IN7 to enter an 8-bit word (D7..D0).

2) Check LED

* If the word is symmetric (palindrome), the LED will turn ON.

* Otherwise, the LED stays OFF.

## External hardware

* 1 LED light
