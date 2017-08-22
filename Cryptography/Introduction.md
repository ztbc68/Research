# What is Cryptography?

Cryp tography = Crypto + graphy
= secret + writing

Cryptography is the science of using secrets to secure communication betweeen two or more parties over an untrusted network.

## Security - What does it mean?
- Confidentiality: Only authorized parties learn the content of communication
- Integrity: No unauthorized party can alter the data
- Authentication: Two communicating participants should be able to identify each other
- Non-repudiation: A participant should not be able to deny previous commitments <br>EX: If you sold something already, you can't change that.

There are many techniques used to achieve these four goals and these techniques can be evaluated with respect to:
- Level of security
- Functionality
- Performance and Implementation details
# Classical Cryptography Systems
## Confidentiality
- Two parties, Alice and Bob, wish to send a secret message to each other
- Alice and Bob share some initial secret k. This initial secret is called a key
- It Alice wants to send a secret message m, she encrypts m using k producing a new message c
The message m is called plaintext and c is called ciphertext
- Alice send c to Bob. Bob can obtain m from c using k.
This process is called decryption

The set of keys, plaintexts and ciphertexts will be denoted by K, M and C respectively. The set of keys K is said to be the keyspace

Kerckhoff's principle = most important principle <br>
No security by obscurity <br>
The security of a cryptosystem should rely on secrecy of k and NOT on secrecy of algorithms used
- Easier to maintain secrecy of keys
- Easier to replace a key, if the key is compromised
- Easier to manage keys amongst many pairs of parties
- Public scrutiny can expose weaknesses of an encryption scheme faster
- Helps establish standards

Attack scenarios <br>
Ciphertext-only attack (COA) <br>
Attacker observes a ciphertext (or sequence of ciphertexts) and tries to find the underlying plaintext (or sequence of plaintexts) <br><br>
Known-plaintext attack (KPA) <br>
Attacker learns pairs (m<sub>1</sub>, c<sub>1</sub>), ..., (m<sub>r</sub>, c<sub>r</sub>) s.t. c<sub>i</sub>
