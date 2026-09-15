# Monero — Blockchain, Privacy & Applied Cryptography

An analysis of **Monero (XMR)** developed for the **Blockchain and Distributed Ledger Technologies** course at **Sapienza University of Rome**, as part of the Master's degree in Cybersecurity.

The project examines how a permissionless blockchain can validate transactions while protecting information about senders, recipients, and transferred amounts. The resulting paper, *Monero: a privacy-focused cryptocurrency*, connects the protocol's cryptographic foundations with its consensus mechanism, economic incentives, governance, and regulatory challenges.

**Author:** Andrea Altomare

📄 **[Read the full paper](Monero_BCeDLT_2025.pdf)** for protocol walkthroughs, mathematical explanations, comparative metrics, and references.

## Project Overview

The goal was to understand Monero as a complete distributed system: how its components work, which privacy and security properties they aim to provide, and where their assumptions and limitations matter. The analysis combines technical literature, protocol documentation, and published security research, moving from blockchain fundamentals to advanced cryptographic constructions and network privacy.

## Privacy & Cryptographic Foundations

The technical core explores how several complementary mechanisms support Monero's **privacy by default** design:

| Area | Topics examined |
| --- | --- |
| **Recipient privacy** | Stealth addresses, one-time output keys, and subaddresses; the roles of private view and spend keys in address derivation and transaction discovery. |
| **Amount confidentiality** | Ring Confidential Transactions (**RingCT**), **Pedersen commitments**, and homomorphic balance verification; **Bulletproofs+** zero-knowledge range proofs for validating hidden amounts. |
| **Sender privacy** | **Ring signatures** and the **CLSAG** scheme, decoy selection, and anonymity sets; **key images** for detecting double spending without identifying the real input within a ring. |
| **Network privacy** | **Dandelion++** transaction propagation, its stem and fluff phases, and the role of **Tor** and **I2P** in reducing exposure of transaction origins and network metadata. |
| **Mathematical foundations** | **Elliptic Curve Cryptography (ECC)** over Edwards25519, **Elliptic Curve Diffie–Hellman (ECDH)**, and the **Elliptic Curve Discrete Logarithm Problem (ECDLP)**, with supporting derivations in the appendix. |

## Architecture, Economics & Governance

The paper places these mechanisms within the broader blockchain ecosystem, covering:

- **Distributed consensus:** Proof of Work, probabilistic finality, and **RandomX**, including its memory-intensive design and approach to ASIC resistance.
- **Development and governance:** CryptoNote origins, Monero's evolution, the Monero Research Lab, and community participation through the Community Crowdfunding System.
- **Cryptoeconomics:** Tail emission, mining incentives, the security budget, dynamic block sizes, transaction fees, and the relationship between privacy and fungibility.
- **Tools and ecosystem:** The `monerod` daemon, wallet clients, JSON-RPC interfaces, and privacy and trust trade-offs across wallet architectures.
- **Regulation and ethics:** Financial privacy, **AML/KYC** requirements, exchange delistings, and the tensions between transaction confidentiality and regulatory oversight.
- **Comparison with Bitcoin:** Ledger transparency, transaction design, mining hardware, monetary policy, and decentralization metrics such as the Nakamoto coefficient.

## Security Analysis & Research Directions

The study also examines where privacy protections can fail or weaken: historical key-image validation vulnerabilities, statistical traceability, decoy-pool manipulation through **Black Marble** flooding, and network-layer deanonymization. Related research extends the discussion to **Full-Chain Membership Proofs (FCMP)** and the quantum threat to elliptic-curve cryptography.

This connects **blockchain security**, **privacy-enhancing technologies**, and **applied cryptography** with adversarial analysis: understanding both the intended guarantees of a protocol and the implementation, statistical, and operational conditions on which they depend.

The paper reflects the sources and protocol context examined in **February 2026**; its regulatory discussion, comparative metrics, and proposed developments should be read in that context.

For the complete analysis and bibliography, see **[Monero: a privacy-focused cryptocurrency](Monero_BCeDLT_2025.pdf)**.
