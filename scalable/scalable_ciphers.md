
# Bitarrays Based Ciphers

## Implementing RSA and ElGamal Ciphers Using Bitarrays

### RSA Cipher with Bitarrays
**Explanation in Natural Language:**  
The RSA cipher implementation with bitarrays involves generating public and private keys from two distinct prime bitarrays `p` and `q`. The public key is a tuple `(n, e)`, and the private key is `(n, v)`, where `n` is the product of `p` and `q`, and `e` and `v` are derived using the extended Euclidean algorithm.

**Pseudo-Code for Key Generation:**
```
Function GenerateKeysRSA(p, q)
    Calculate n = p * q and phi = (p-1) * (q-1)
    Find a co-prime e to phi using extended Euclidean algorithm
    Calculate private key component v
    Return public key (n, e) and private key (n, v)
End Function
```

**Pseudo-Codes for Encryption and Decryption:**
```
Function EncryptRSA(m, pub_key)
    Perform modular exponentiation of m with public key components
End Function

Function DecryptRSA(m, priv_key)
    Perform modular exponentiation of m with private key components
End Function
```

### ElGamal Cipher with Bitarrays
**Explanation in Natural Language:**  
ElGamal encryption using bitarrays requires generating public data `(g, p)` and keys. The public key is a bitarray `h` and the private key is `x`. Encryption involves modular arithmetic operations on the message and public data, while decryption uses the private key and the encrypted message.

**Pseudo-Code for Key Generation:**
```
Function GenerateKeysG(g, p)
    Select a private key x and calculate public key h
    Return (h, x)
End Function
```

**Pseudo-Codes for Encryption and Decryption:**
```
Function EncryptG(msg, pub_data, kA)
    Encrypt msg using public data and ElGamal public key
End Function

Function DecryptG(msg, a, pub_data)
    Decrypt the message using private key and public data
End Function
```

**Fact:** RSA and ElGamal ciphers are fundamental in public-key cryptography, securing digital communication by enabling secure key exchanges and data encryption.

**Tip:** Efficient implementation of these ciphers, especially using bitarrays, is crucial for handling large numbers typically used in cryptographic applications.
