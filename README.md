# Q-Ledger: Quantum-Safe Integrity for Land Records

## Overview

Q-Ledger is a prototype demonstrating how post-quantum digital signatures and a SHA-256 hash-linked ledger can help verify the integrity of sample land records and detect unauthorized modifications.

## Objective

Demonstrate record signing, signature verification, hash linking, and tamper detection using post-quantum cryptography.

## Features

- Processes 1,000 sample land records.
- Uses ML-DSA-65 digital signatures to verify record authenticity and detect changes to signed data.
- Uses SHA-256 to generate record hashes and link ledger entries.
- Tests original and modified records.
- Exports verification results in CSV and JSON formats.
- Generates a visualization of verification results.

## Technologies Used

- Python
- Pandas
- `cryptography` library — ML-DSA-65
- SHA-256
- Jupyter Notebook
- Matplotlib

## Results

In the recorded test run:

- Records processed: 1,000
- Valid signatures: 1,000
- Invalid signatures: 0
- Original hash-linked ledger: Valid
- Tampered ledger: Invalid
- Modified-record signature test: Passed; the modified record was rejected

These results describe the tested sample dataset and local prototype, not a production deployment.

## How It Works

1. Load and preprocess the sample land-record dataset.
2. Canonicalize the selected record fields into a consistent representation.
3. Generate an ML-DSA-65 signature for each record.
4. Verify signatures against the corresponding record data.
5. Generate SHA-256 record hashes and link ledger entries using previous-entry hashes.
6. Modify test data and verify that integrity checks detect the changes.
7. Export audit results and a verification summary.

## Dataset

The prototype uses a 1,000-row Tamil Nadu sample land-record dataset. It must not be represented as official government data unless its provenance has been independently verified.

## Limitations and Future Work

This is a local proof-of-concept, not a production land registry or a fully distributed blockchain.

Future work includes:

- Secure, persistent private-key management and trusted public-key distribution.
- Multi-node replication and consensus.
- Access control and privacy-preserving data handling.
- Testing with larger datasets and independently validated records.
- Protecting ledger checkpoints against unauthorized rewriting.

## Security Note

ML-DSA-65 is a post-quantum digital signature algorithm, while SHA-256 is a cryptographic hash function. They serve different purposes. The current prototype demonstrates selected integrity checks; it does not establish that a complete land-record system is quantum-safe or production-ready.

Do not publish private keys, sensitive owner information, or identifiable raw records in a public repository.
