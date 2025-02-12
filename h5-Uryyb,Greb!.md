# H5 Homework

## X) Summaries

### <ins>Applied Cryptography: Chapter 1</ins>   

- 

<ins>Subtitle</ins> 
-
<ins>References</ins> 
- 


### <ins>PGP – Send Encrypted and Signed Message</ins>  

- The article demonstrates Asymmetric encryption (using PGP) by simulating two users.

<ins>Basic concepts</ins>   
- Data sent over the internet can be intercepted, modified, or viewed by unauthorized parties. Encryption and signing are used to protect messages sent over untrusted connections. 
- Encryption protects data by converting it into an unreadable format.
- Signing uses digital signatures to protect data from modification and confirms the sender’s identity.

- PGP is a highly secure encryption standard which is used for encrypting and signing messages. 
- GPG (GNU privacy guard) is a tool for using PGP encryption

- Asymmetric/ Public key encryption uses a keypairs - public keys (shared publicly) and private keys (kept private) – to establish trust between senders and recipients. Both parties generate a key pair from which public keys are exchanged. The exchanged keys are used for both message encryption and verification of the sender’s identity (signature). 
- Public key is used for:
  - Encryption
  - Verifying signatures
  - Sending (encrypted) messages (recipient’s public key)
- Private key is used for:
  - Decryption
  - Signing messages

- Key management/protection is important. Losing or leaking the private key compromises security. In such a case, the private key should be disabled in all services using it.  


<ins>Steps for establishing trust in Asymmetric Encryption </ins> 
- Note: related commands are shown in exercise c)

1. Generate key pair (both parties)
2. Exchange public keys (over untrusted channels):
  a) Export your public key and share it to the source from which you want to receive messages
  b) Import the public key of the other party.  
3. Verify that the public key belongs to the appropriate party and sign it as trusted. Keys can be verified with fingerprints, associated email addresses or signatures from trusted third parties.

<ins>Steps for sending messages in Asymmetric Encryption</ins> 
- Note: related commands are shown in exercise c)

1. Generate message
2. Encrypt the message using the recipient’s public key
3. Sign the message using your own private key. (This signature is used by the recipient to verify sender’s identity. The verification on the recipient side uses the sender’s public key which was exchanged in trust establishment).
Note: Only recipient’s private key can decrypt the message after this point (recipient’s matching pub-priv key pair).
Only recipient’s private key can decrypt the message after this point (recipient’s matching pub-priv key pair )
4. Send message to recipient over an untrusted channel.

<ins>Steps for receiving messages in Asymmetric Encryption</ins> 
- Note: related commands are shown in exercise c)

1. Decrypt message private key
2. Verify sender’s signature with sender’s public key (which was exchanged earlier in trust establishment)


<ins>References</ins> 
- Karvinen 2023: PGP - Send Encrypted and Signed Message – gpg at https://terokarvinen.com/2023/pgp-encrypt-sign-verify/ 
