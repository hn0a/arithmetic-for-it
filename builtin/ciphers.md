
# Ciphers: Integer-Based Encryption Techniques

## Implementing Various Ciphers in OCaml

### Cesar Cipher
**Explanation in Natural Language:**  
The Caesar cipher is a simple encryption technique where each letter in the plaintext is shifted a certain number of places down or up the alphabet. This implementation takes an integer key `k`, a word `m` to cipher, and a base `b`, typically 256 for ASCII codes. Each character in `m` is shifted by `k` places modulo `b`.

**Pseudo-Code for Encryption:**
```
Function EncryptCesar(k, m, b)
    For each character e in m
        Shift e by k places modulo b
    Return the encrypted message
End Function
```

**Pseudo-Code for Decryption:**
```
Function DecryptCesar(k, m, b)
    For each character e in m
        Shift e by -k places modulo b
    Return the decrypted message
End Function
```

### RSA Cipher
**Explanation in Natural Language:**  
RSA is a widely-used public-key cryptosystem. The `generate_keys_rsa` function creates a pair of public and private keys from two prime numbers `p` and `q`. The encryption and decryption functions use modular exponentiation to secure the data.

**Pseudo-Code for Key Generation:**
```
Function GenerateKeysRSA(p, q)
    Calculate n = p * q and phi = (p-1) * (q-1)
    Find a co-prime e to phi
    Calculate the private key d using extended Euclidean algorithm
    Return public key (n, e) and private key (n, d)
End Function
```

**Pseudo-Code for Encryption and Decryption:**
```
Function EncryptRSA(m, pub_key)
    Return mod_power of m with pub_key
End Function

Function DecryptRSA(m, priv_key)
    Return mod_power of m with priv_key
End Function
```

### ElGamal Cipher
**Explanation in Natural Language:**  
ElGamal is another form of public-key cryptography. The `generate_keys_g` function generates public and private keys based on prime numbers and primitive roots. Encryption and decryption involve modular arithmetic operations.

**Pseudo-Code for Public Data and Key Generation:**
```
Function GeneratePublicDataG(p)
    Find a prime q such that p = 2*q + 1
    Return (g, p)
End Function

Function GenerateKeysG(g, p)
    Select a private key x
    Calculate public key h
    Return (h, x)
End Function
```

**Pseudo-Code for Encryption and Decryption:**
```
Function EncryptG(msg, pub_data, kA)
    Select a random number r
    Calculate c1 and c2 using modular operations
    Return (c1, c2)
End Function

Function DecryptG(msg, a, pub_data)
    Perform modular operations to decrypt msg
    Return decrypted message
End Function
```

**Fact:** Cryptography is a constantly evolving field, with techniques like RSA and ElGamal being fundamental to modern secure communication.

**Tip:** Understanding these cryptographic algorithms is essential for anyone interested in cybersecurity, as they form the basis for many of today's secure communication protocols.

