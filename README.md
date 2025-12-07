## Objective
The aim of this assignment is to extract the elliptic curve equation and the finite field characteristic from a website's SSL certificate that uses ECDSA.

## How the Code Works

1. The program begins by loading the SSL certificate file using the `cryptography` library.

2. It extracts the **public key** from the X.509 certificate.

3. The program checks whether the public key is based on **Elliptic Curve Cryptography (ECC)**.

4. If ECC is detected, the program reads:
   - The elliptic curve name
   - The key size

5. The extracted curve name is then matched with predefined standard curves
   inside a dictionary.

6. Based on the curve name, the program prints:
   - Elliptic curve equation
   - Finite field characteristic
   - Field type

7. If the curve is not present in the dictionary, the program notifies the user
   that the curve information is not available in the database.

This ensures the certificate's elliptic curve parameters are decoded and displayed in a human-readable mathematical format.

# PA-2: Extracting Elliptic Curve Information from SSL Certificate

## Tools Used
- Python 3
- cryptography Python library

## Input
An SSL certificate file (.crt) downloaded from a website using ECDSA.

## Output
- Elliptic curve name
- Key size
- Elliptic curve equation
- Characteristic of finite field

## Extracted Result

Curve Name: secp384r1  
Key Size: 384 bits  

Elliptic Curve Equation:
y² = x³ − 3x + b (mod p)

Finite Field Characteristic:
p = 2^384 − 2^128 − 2^96 + 2^32 − 1

Field Type:
Prime Field (Fp)

