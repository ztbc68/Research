# Classical Cryptography Systems
## Confidentiality
- Two parties, Alice and Bob, wish to send a secret message to each other
- Alice and Bob share some initial secret k. This initial secret is called a key
- It Alice wants to send a secret message m, she encrypts m using k producing a new message c
The message m is called plaintext and c is called ciphertext
- Alice send c to Bob. Bob can obtain m from c using k.
This process is called decryption

The set of keys, plaintexts and ciphertexts will be denoted by K, M and C respectively. The set of keys K is said to be the keyspace

## Formally
A symmetric key encryption scheme consists of three algorithms:
1. GEN: A probabilistic algorithm that outputs a key k.
2. enc: Takes as inputs plaintext m and a key k.<br>Outputs a ciphertext c.<br>We write enc<sub>k</sub>(m) for the encryption of m using key k.
3. dec: Takes as input ciphertext c and a key k.<br>Outputs a plaintext m.<br>We write dec<sub>k</sub>(c) for the decryption of m using key k.<br><br>
Fundamental Requirement<br>
dec<sub>k</sub>(enc<sub>k</sub>(m)) = m

## Kerckhoff's Principle
Kerckhoff's principle = most important principle <br>
No security by obscurity <br>
The security of a cryptosystem should rely on secrecy of k and NOT on secrecy of algorithms used
- Easier to maintain secrecy of keys
- Easier to replace a key, if the key is compromised
- Easier to manage keys amongst many pairs of parties
- Public scrutiny can expose weaknesses of an encryption scheme faster
- Helps establish standards

## Attack scenarios
Ciphertext-only attack (COA) <br>
Attacker observes a ciphertext (or sequence of ciphertexts) and tries to find the underlying plaintext (or sequence of plaintexts) <br><br>
Known-plaintext attack (KPA) <br>
Attacker learns pairs (m<sub>1</sub>, c<sub>1</sub>), ..., (m<sub>r</sub>, c<sub>r</sub>) s.t. c<sub>i</sub> = enc<sub>k</sub>(m<sub>i</sub>), for some key k<br>
Then given a new ciphertext c encrypted using k, attacker tries to find the underlying plaintext<br>
- If an encryption scheme is KPA-secure then it is also COA-secure
