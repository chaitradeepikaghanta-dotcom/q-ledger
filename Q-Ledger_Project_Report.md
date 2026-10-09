# Q-Ledger
## Post-Quantum Integrity Verification for Land Records

### 1. Abstract
Q-Ledger is a local prototype exploring post-quantum digital
signatures and hash-linked records for detecting unauthorized
changes to land-record data.

### 2. Dataset
- Records processed: 1000
- Dataset: Tamil Nadu sample land-record dataset.
- Owner mobile-number column removed during preprocessing.
- This is not represented as official Andhra Pradesh government data.

### 3. Technologies
- Python and Pandas
- ML-DSA-65 digital signatures
- SHA-256 hashing
- Jupyter Notebook
- Matplotlib

### 4. Methodology
1. Load and preprocess sample land records.
2. Canonicalize protected record fields.
3. Sign records using ML-DSA-65.
4. Verify digital signatures.
5. Build a hash-linked ledger using SHA-256.
6. Test record and ledger tampering.
7. Export verification and audit results.

### 5. Results
- Records processed: 1000
- Valid signatures: 1000
- Invalid signatures: 0
- Original hash chain valid: True
- Record tampering test: Passed in the notebook.
- Hash-chain tampering test: Modified chain rejected.

### 6. Limitations
This is a local prototype, not a fully distributed blockchain
or production land-registration service. Multi-node replication,
consensus, secure private-key management, trusted public-key
distribution, access control, and validation against official
registry data remain future work.

### 7. Conclusion
The prototype demonstrates record signing, signature verification,
hash-linked ledger construction, and detection of tested
modifications. Further work is required for a secure distributed
deployment.

### 8. Responsible Data Handling
Do not publish identifiable landowner information or private keys.
Clearly state the dataset provenance in any public presentation.
