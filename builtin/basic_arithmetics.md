
# Algorithms Explained

## 1. Algorithm for Greatest Common Divisor (GCD)

**Explanation in Natural Language:**  
This algorithm calculates the greatest common divisor (GCD) of two non-zero integers. It employs the approach of the Euclidean algorithm, which is based on recursion. The principle is straightforward: the GCD of two numbers `a` and `b` is the same as the GCD of `b` and the remainder of `a` divided by `b`. The algorithm continues this operation, swapping the numbers and calculating the new remainder, until one of the numbers becomes zero. At that point, the other number is the GCD.

**Pseudo-Code:**
```
Function GCD(a, b)
    While b ≠ 0
        temp ← b
        b ← a mod b
        a ← temp
    End While
    Return a
End Function
```

**Fact:** The Euclidean algorithm is one of the oldest known algorithmic techniques, used since ancient times.

## 2. Extended Euclidean Division Algorithm

**Explanation in Natural Language:**  
This method extends the classic Euclidean division. For two non-zero integers, the algorithm finds three values: `u`, `v`, and `d`, such that `a*u + b*v = d`, where `d` is the GCD of `a` and `b`. The algorithm operates recursively, progressively reducing the values of `a` and `b`. When `a` reaches zero, the process concludes, and the values of `u` and `v` are calculated on the way back up the recursion. These values are significant because they have practical applications, particularly in computing modular inverses in cryptography.

**Pseudo-Code:**
```
Function ExtendedEuclideanDivision(a, b)
    If a = 0
        Return (0, 1, b)
    End If
    (x1, y1, gcd) ← ExtendedEuclideanDivision(b mod a, a)
    x ← y1 - (b / a) * x1
    y ← x1
    Return (x, y, gcd)
End Function
```

**Tip:** The extended Euclidean division is essential in many fields, especially in cryptography, for its applications in calculating modular inverses, a critical component in encryption algorithms like RSA.
