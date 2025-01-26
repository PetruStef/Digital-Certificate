# Overview
This project implements a comprehensive digital certificate system modeled on the X.509 standard to secure communication over unsecured channels. It includes functionalities for:
•	Generating a self-signed root certificate.
•	Issuing derived certificates.
•	Managing certificate revocation through a Certificate Revocation List (CRL).
•	Handling certificate expiration and renewal.
•	Integrating certificates with key exchange for symmetric encryption.

# Project Structure

This document outlines the directory structure and purpose of each component in the digital certificate system project.

```
project/
├── certificates/         # Stores generated certificates and private keys
├── crl/                  # Stores the Certificate Revocation List (CRL)
├── docs/                 # Contains project documentation
├── src/                  # Source code for the project
│   ├── generate_crl.py          # Script for generating CRLs
│   ├── generate_root.py         # Script for generating the root certificate
│   ├── issue_certificate.py     # Script for issuing certificates
│   ├── key_exchange.py          # Handles key exchange functionality
│   ├── renew_certificate.py     # Script for renewing certificates
│   ├── revoke_certificate.py    # Handles revocation of certificates
│   ├── symmetric_encryption.py  # Implements symmetric encryption
│   ├── verify_certificates.py   # Validates certificates
├── valid/               # May contain validation-related data or scripts
└── README.md            # Project overview and instructions
```

## Directory Descriptions

1. **`certificates/`**:
   - Contains generated certificates (e.g., root, derived) and private keys in PEM format.

2. **`crl/`**:
   - Stores Certificate Revocation List (CRL) files, which list revoked certificates.

3. **`docs/`**:
   - Project documentation, including technical details and implementation notes.

4. **`src/`**:
   - Source code for all functionality in the project.
   - Key scripts:
     - `generate_root.py`: Generates the root certificate.
     - `issue_certificate.py`: Issues derived certificates.
     - `generate_crl.py`: Creates the Certificate Revocation List.
     - `revoke_certificate.py`: Adds revoked certificates to the CRL.
     - `renew_certificate.py`: Handles certificate renewal before expiration.
     - `key_exchange.py`: Performs key exchange (ECDH).
     - `symmetric_encryption.py`: Encrypts and decrypts data using AES.
     - `verify_certificates.py`: Validates certificates for expiration, signature, and revocation.

5. **`valid/`**:
   - Placeholder for validation data or scripts, if applicable.

6. **`README.md`**:
   - Contains an overview of the project and usage instructions.
