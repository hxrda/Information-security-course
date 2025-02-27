# H6 Homework

## X) Summaries

### <ins>Applied Cryptography: Chapter 2.3 - One-Way Functions</ins>   

<ins>Basics of one-way functions</ins>  
- A one-way function is a function which is easy to compute but difficult to reverse.
  - Given x, computing f(x) is easy. However, given f(x), computing x is difficult even with unlimited time and computing power.  

<ins>One-way functions & cryptography</ins>  
- One-way functions by themselves are not useful for encryption as they cannot be decrypted. 
- A trapdoor one-way function is a special type of one-way function which is hard to compute in reverse unless a secret piece of information, a “trapdoor”, is known. Thus, a trapdoor one-way function enables both encryption and decryption.
  - Given f(x) and y, it will be easy to compute x.
  - 
- Trapdoor one-way functions are the foundation of public-key cryptography.


### <ins>Applied Cryptography: Chapter 2.4 - One-Way Hash Functions</ins>   

### <ins>References:</ins>  
- Schneier, B. 2015: Applied Cryptography: Chapter 2: Protocol Building Blocks. O’Reilly Online Learning. Available at: https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02-sec001 

## A) Install Hashcat. Test it with a sample hash

<ins>References</ins>
- Karvinen 2023: PGP - Cracking Passwords with Hashcat at https://terokarvinen.com/2022/cracking-passwords-with-hashcat/ 

## B) Crack the hash: d595b2086532422bbe654bc07ea030df

<ins>References</ins>
