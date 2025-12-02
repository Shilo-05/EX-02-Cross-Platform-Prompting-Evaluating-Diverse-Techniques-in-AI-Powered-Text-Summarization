# EX-02-Cross-Platform-Prompting-Evaluating-Diverse-Techniques-in-AI-Powered-Text-Summarization

```text
Name:    Oswald Shilo
Reg.No:  212223040139
```

## AIM
To evaluate and compare the effectiveness of prompting techniques (zero-shot, few-shot, chain-of-thought, role-based) across different AI platforms (ChatGPT, Gemini, Claude, Copilot) in the task of text summarization.

## SCENARIO
You are part of a content curation team for an educational platform that delivers quick summaries of research papers to undergraduate students. Your task is to summarize a 500-word technical article on "The Basics of Blockchain Technology" using multiple AI platforms and prompting strategies to find the most efficient workflow.

## ALGORITHM

### 1. Article Selection
**Input Text (approx. 500 words):**
> *Blockchain technology is fundamentally a distributed, decentralized ledger that records transactions across a network of computers. Unlike traditional databases managed by a central authority (like a bank or government), a blockchain allows multiple parties to share a single, immutable history of information. The technology was first introduced in 2008 by Satoshi Nakamoto as the underlying infrastructure for Bitcoin, solving the "double-spending" problem without requiring a trusted intermediary.*
>
> *At its core, a blockchain consists of a chain of digital "blocks" that contain data. Each block holds a specific set of information: valid transaction records, a timestamp, and a cryptographic hash of the previous block. This hash acts like a digital fingerprint. If anyone attempts to alter the data in a block, the hash changes completely. Since the next block in the chain carries the previous block’s hash, any tampering breaks the chain, making the corruption immediately evident to the entire network.*
>
> *The security of the blockchain relies on a consensus mechanism, such as "Proof of Work" (used by Bitcoin) or "Proof of Stake." In Proof of Work, powerful computers (miners) compete to solve complex mathematical puzzles to validate transactions and create new blocks. This process requires significant energy but ensures that rewriting the ledger is computationally infeasible for any single attacker. Once a block is added, it cannot be changed, ensuring data immutability.*
>
> *Beyond cryptocurrencies, blockchain has potential applications in various sectors. In supply chain management, it provides end-to-end transparency, allowing consumers to trace the origin of products. In healthcare, it can securely store patient records that are accessible only to authorized providers. Smart contracts—self-executing contracts with the terms directly written into code—automate processes on platforms like Ethereum, reducing the need for lawyers or notaries.*
>
> *However, the technology faces challenges. Scalability is a major issue; public blockchains can be slow and expensive to use during peak times. Additionally, the regulatory environment remains uncertain in many jurisdictions. Despite these hurdles, blockchain represents a paradigm shift in how digital trust is established and maintained.*

### 2. Prompt Design
* **Zero-shot:** "Summarize the following text in simple terms for undergraduate students."
* **Few-shot:** [Provided two examples of technical summaries on "Cloud Computing" and "AI Ethics" before the target text].
* **Chain-of-thought:** "First, identify the main definition of blockchain. Second, list the key technical components (blocks, hashes, consensus). Third, mention applications and challenges. Finally, combine these points into a coherent summary."
* **Role-based:** "You are a Computer Science Professor explaining this concept to a freshman class. Use analogies and keep the tone educational but accessible."

### 3. Execution & Simulation (Sample Outputs)

| Platform + Strategy | Sample Output Snippet | Observations |
| :--- | :--- | :--- |
| **ChatGPT (Zero-shot)** | "Blockchain is a shared digital ledger used to record transactions across many computers so that the record cannot be altered retroactively. It was invented for Bitcoin but has uses in supply chains and healthcare..." | Fast, simple, but missed the "hash" explanation. |
| **Gemini (Few-shot)** | "Similar to our previous examples, Blockchain is a decentralized technology ensuring data integrity. **Key mechanism:** It uses cryptographic hashes to link blocks. **Applications:** Supply chain, smart contracts..." | Structured well, followed the "problem-solution" format of the few-shot examples. |
| **Claude (Chain-of-thought)** | "1. **Core Concept:** Distributed ledger. 2. **Mechanism:** Blocks linked by hashes prevent tampering. 3. **Consensus:** Proof of Work secures the network. **Summary:** Blockchain is a secure, decentralized way to record data. By linking data blocks with unique digital fingerprints, it creates an unchangeable history useful for finance and healthcare..." | Highly logical flow; effectively connected the "how" (hashes) to the "why" (security). |
| **Copilot (Role-based)** | "Imagine a shared Google Doc that once you type in, you can never delete. That is Blockchain! As your professor, I want you to understand that instead of a bank keeping the ledger, everyone keeps a copy..." | Very engaging and relatable, though it slightly oversimplified the consensus mechanism. |

### 4. Evaluation
*Scale: 1 (Poor) to 5 (Excellent)*

| Platform | Strategy | Accuracy | Coherence | Simplicity | Speed | User Exp | **Avg Score** |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **ChatGPT** | Zero-shot | 4 | 5 | 5 | 5 | 5 | **4.8** |
| **Gemini** | Few-shot | 5 | 4 | 4 | 4 | 4 | **4.2** |
| **Claude** | Chain-of-Thought | 5 | 5 | 4 | 3 | 4 | **4.2** |
| **Copilot** | Role-based | 3 | 5 | 5 | 4 | 5 | **4.4** |

### 5. Comparison and Ranking
* **Accuracy:** Claude (CoT) and Gemini (Few-shot) tied for highest accuracy.
* **Speed:** ChatGPT (Zero-shot) was the fastest.
* **Engagement:** Copilot (Role-based) had the best user engagement but lower technical precision.

## RESULT
* The results showed that **Claude combined with Chain-of-Thought prompting** delivered the most effective summaries for educational purposes. This combination excelled in accuracy, logical flow, and maintaining clarity, especially when simplifying technical terms like "cryptographic hash."
* **ChatGPT with zero-shot prompting** was the fastest, producing quick summaries that were generally accurate and simple, though they sometimes lacked depth regarding specific mechanisms.
* **Gemini with few-shot prompting** provided solid results, mirroring the structure of provided examples well. However, the setup time was longer due to the need to input examples.
* **Copilot using role-based prompting** was the easiest to interact with and produced the most relatable analogies, but occasionally lost technical accuracy due to over-simplification.

Video: [Prompt Engineering for Summarization](https://www.youtube.com/watch?v=A_s4wR3tKkk)
