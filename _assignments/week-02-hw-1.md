---
title: Representing Floating Point Numbers
week: 2
homework: 1
source: 05S1 CS115 - Taught by Dan Duchamp
---

1. Consider a simple 16-bit floating point format that uses one bit to indicate sign (1 means negative), 11 bits for the mantissa, and 4 bits for an exponent stored in two’s complement format. The bits are stored left to right in the above order; i.e., the sign bit is leftmost and the exponent bits are rightmost. What numbers are represented by these bits?
    * `1101 0100 0000 0110` 
    * `0000 0000 0001 1000`
    * `0000 0000 0000 0000`
    
2. Using the above floating point format, write the binary representation for these decimal numbers.  (**Note**: some of these numbers may not be representable in binary.  If so, please state that fact and use the closest approximation you can create in this 16-bit format):
    * -0.125
    * 4.5
    * 1/3
    * 0.1
    
3. Choose three more decimal numbers and write their floating point binary representations.
