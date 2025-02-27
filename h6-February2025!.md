# H6 Homework

## X) Summaries

### <ins>Applied Cryptography: Chapter 2.3 - One-Way Functions</ins>   

<ins>Definition of one-way functions</ins>  
- A one-way function is a function which is easy to compute but difficult to reverse.
  - Given x, computing f(x) is easy. However, given f(x), computing x is difficult even with unlimited time and computing power.  

<ins>One-way functions & cryptography</ins>  
- One-way functions by themselves are not useful for encryption as they cannot be decrypted. 
- A trapdoor one-way function is a special type of one-way function which is hard to compute in reverse unless a secret piece of information, a “trapdoor”, is known. Thus, a trapdoor one-way function enables both encryption and decryption.
  - Given f(x) and y, it will be easy to compute x.
    
- The concept of trapdoor one-way functions are at the foundation of public-key cryptography.
    

### <ins>Applied Cryptography: Chapter 2.4 - One-Way Hash Functions</ins>   

<ins>Definition of hash functions</ins>
- Hash functions take variable-length input strings (pre-image) and convert them to fixed-length output strings (hash value).
- The hash value “fingerprints” the pre-image. Since several inputs can produce the same hash, the fingerprints are not entirely unique. However, they provide a “good-enough” assurance of accuracy for practical purposes.

<ins>Definition of one-way hash functions</ins>
- A one-way hash function works in one direction, where it is easy to compute a hash value from a pre-image but hard to reverse the process.
- Aka:
  - Compression function, Contraction function, Message digest, Fingerprint, Cryptographic checksum, Message integrity check (MIC), and Manipulation detection code (MDC).

<ins>Characteristics of one-way hash functions</ins>
- One-wayness: It’s easy to compute the hash, but unfeasible to reverse the process. The output is not dependent on the input in any observable way
- Publicity: The function’s security relies on its one-wayness and not the process itself. Information about the hash function is publicly disclosed.
- Avalanche effect: A slight change in input results in a significant change in the output (hash value)
- Collision-free: It is difficult to find different inputs/pre-images that result in same hash output. Good one-way hash functions are collision-free. 

<ins>One-way hash functions & keys</ins>
- Using keyless one-way hash functions allow anyone to compare and verify the hashes.
- Message or data authentication codes (MACs/DACs) are an enhanced version of the one-way hash function which include a secret key. The hash value is the function of both the pre-image and the key. Only someone with the correct key can verify the hash value.

<ins>One-way hash functions & cryptography</ins>  
- One-way hash functions are the foundation of modern public-key cryptography.


### <ins>References:</ins>  
- Schneier, B. 2015: Applied Cryptography: Chapter 2: Protocol Building Blocks. O’Reilly Online Learning. Available at: https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02-sec001 

## A) Install Hashcat. Test it with a sample hash

<ins>References</ins>
- Karvinen 2023: PGP - Cracking Passwords with Hashcat at https://terokarvinen.com/2022/cracking-passwords-with-hashcat/ 

## B) Crack the hash: d595b2086532422bbe654bc07ea030df

<ins>References</ins>
