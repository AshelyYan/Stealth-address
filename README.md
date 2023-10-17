# Stealth-address
Ensuring privacy within the Blockchain ecosystem presents a substantial challenge. To address the challenge of pseudonymity in traditional blockchain transactions, various privacy-preserving techniques have emerged, such as Zero-Knowledge Proofs \cite{blum2019non}, encryption schemes, Stealth Address (SA) and so on. Among all of these, introducing the concept of SA as a centric solution for privacy-preserving transaction is noteworthy. Based on the Diffie-Hellman key exchange protocol \cite{diffie2022new}, SA can help protect the privacy of users by making it extremely difficult for outsiders to link a transaction to a specific individual or entity. This is particularly important as blockchain ledgers are public and anyone can inspect them. They achieve this by generating unique, one-time addresses for each transaction, making it challenging for external parties to track or analyze financial activity on the blockchain. 

Nowadays, one of the most widely embraced SA schemes is the Dual-Key Stealth Address Protocols (DKSAP) \cite{courtois2017stealth}, which introduces a noteworthy enhancement by incorporating multiple distinct spending keys into the protocol. 
This strategic addition serves to fortify the protocol's resilience against potential attacks like the “bad random attack” or situations where keys become compromised, where it separates the root keys into viewing keys and spending keys to reduce the risk of the root key. While this advancement offers enhanced security, it does come with the risk of viewing key leakage and vulnerability to quantum computing attacks. We conclude that the current SA schemes face three primary issues: key leakage attacks, scalability and usability concerns, and vulnerability to quantum computing attacks.

## FHE-DKSAP
To overcome these challenges, we propose the verifiable anonymization transaction scheme, the combination of Zero knowledge proof with HE-DKSAP (homomorphic encryption based dual key stealth address protocol) to provide a verifiable scheme while maintaining strong privacy guarantees. The main contribution of this proposal includes the follows.

1. We use zero-knowledge proof to verify both the transfer and receive without revealing the details of the transaction. These attached proofs can demonstrate that their funds (are not) derived from known (il)legal sources.
    
2. HE-DKSAP replaces elliptic curve with homomorphic encryption to improve security level. Fully homomophic encryption constructs the lattice cryptographic, and born to equip fully HE-DKSAP to prevents quantum computing attacks. Therefore, SA in fully HE-DKSAP is secured to be reused and no need to generate large amount of SA to reduce the complexity and difficulty of SA adoption.
    
3. Compared to the dual-key design in DKSAP, our HE-DKSAP design can mitigate the temporary key leakage issue by exclusively sharing data through the ciphertext.
    
4. HE-DKSAP allows for the reuse of the recipient's public key, which not only reduces the complexities of key management but also eliminates the necessity for an ever-growing number of keys.

We provide the codes for the implementation of FHE-DKSAP and meanwhile provide some of the experiemnt results for it. 
