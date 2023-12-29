
# A Naive Implementation of Big Integers

## Implementing Bitarrays in OCaml for Big Integer Arithmetic

### Creating a Bitarray from a Built-In Integer
**Explanation in Natural Language:**  
The function `from_int` converts a built-in integer to a bitarray, which is a list of zeros and ones representing the binary form of the integer. The first bit indicates the sign, followed by bits representing the integer in binary, read from left to right.

**Pseudo-Code:**
```
Function FromInt(x)
    Convert x into its binary representation
    If x is negative, start with 1 (sign bit) followed by binary form of -x
    Else start with 0 (sign bit) followed by binary form of x
End Function
```

### Transforming Bitarray to Built-In Integer
**Explanation in Natural Language:**  
The `to_int` function transforms a bitarray back into a built-in integer. It interprets the bitarray as a binary number, with the first bit as the sign bit, and computes the corresponding integer value.

**Pseudo-Code:**
```
Function ToInt(bA)
    Interpret bA as a binary number with the first bit as sign
    Compute and return the corresponding integer
End Function
```

### Comparing Bitarrays
**Explanation in Natural Language:**  
Various comparison functions (`compare_b`, `>>`, `<<`, etc.) are provided to compare two bitarrays. These functions interpret bitarrays as binary numbers and perform comparisons based on their represented values.

**Pseudo-Codes for Comparisons:**
```
Function CompareB(bA, bB)
    Compare two bitarrays as binary numbers
    Return 1, -1, or 0 based on the comparison
End Function

Function BiggerThan(bA, bB)
    Return true if bA represents a bigger number than bB
End Function
```

### Arithmetic Operations on Bitarrays
**Explanation in Natural Language:**  
Arithmetic operations such as `add_b`, `diff_b`, `mult_b`, etc., perform addition, subtraction, multiplication, and division on bitarrays. These functions handle binary arithmetic according to the defined conventions for bitarrays.

**Pseudo-Codes for Arithmetic Operations:**
```
Function AddB(bA, bB)
    Perform binary addition on two bitarrays
    Return the resulting bitarray
End Function

Function MultB(bA, bB)
    Perform binary multiplication on two bitarrays
    Return the resulting bitarray
End Function
```

**Fact:** Implementing big integers as bitarrays allows for handling numbers larger than standard integer types, crucial for certain applications like cryptography.

**Tip:** Understanding binary arithmetic and its implementation is key to efficiently manipulating large integers in low-level programming and algorithm design.

