---
title: The ROT-13 Cipher
week: 4
homework: 4
---

ROT-13 is a letter substitution cipher related to the Caesar cipher.  In the Caesar cipher, imagine that you had the letters of the alphabet written around the two circular disks.  By rotating one of the disk, you arrive at a mapping from one letter to another.  With the English 26-character alphabet, ROT-13  is the result of rotating the disk 180 degrees such that each letter of the first half of the alphabet maps to a letter in the second half and vice versa.  The mapping looks like this:

```
A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
| | | | | | | | | | | | | | | | | | | | | | | | | |
N O P Q R S T U V W X Y Z A B C D E F G H I J K L M
```

Because the cipher is symmetrical, the original text can be recovered by applying the ROT-13 cipher to the encrypted text a second time.

Included in the starter project for this assignment is a file `encrypted.txt` that contains a famous passage from a book encrypted using the ROT-13.  Your task is to fill in the stub methods in the project to read in this file, decrypt it, and write the result to a file called `decrypted.txt`.

Hint: remember from the first week's homework, each character in Java is represented as a number encoded in unicode.  Capital 'A' is the decimal number 65.  Capital 'N' is the decimal number 78.
