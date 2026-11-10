# DSC 180A Methodology Assignment 4

**Name:** Ritvik Chand  
**Email:** rchand@ucsd.edu  
**Section:** D26 
**Mentor:** Lily Weng  

## Quarter 2 Project Proposal Brainstorming

**1. What is the most interesting topic covered in your domain this quarter?**

Something I found pretty interesting was how we can make LLMs more reliable through reflection and self-correction. In addition, I was interested in how RAG systems can still produce hallucinations even when they retrieve relevant documents. Through our work on TrustRAG and related papers, I learned more about how retrieval errors and generation errors can be identified separately. I found this interesting because it shows that improving retrieval accuracy alone isn't always enough to make an LLM's responses trustworthy.

**2. Describe a potential investigation you would like to pursue for your Quarter 2 Project.**

For Quarter 2, I am interested in investigating whether a RAG system can automatically verify that its generated answers are supported by the retrieved documents. One approach that I have thought of would be to build a verification layer that evaluates the relationship between generated claims and their cited evidence. If a claim is unsupported, the system could either retrieve additional documents or revise its response. I would compare this approach against a standard RAG baseline using metrics such as hallucination rate, citation accuracy, and response latency. I would also be interested in understanding whether the improvements in reliability justify the additional computational latency and expense.

**3. What is a potential change you'd make to the approach taken in your current Quarter 1 Project?**

One change I would consider is incorporating hybrid retrieval rather than relying on a single retrieval method. Combining BM25 with dense vector retrieval could help the system identify documents that are relevant both through exact keyword matches and semantic similarity. I would also consider separating the verification and correction stages so that we can evaluate which component actually contributes to improving answer reliability. This would make it easier to understand whether errors originate from retrieval, generation, or the verification process itself.

**4. What other techniques would you be interested in using in your project?**

I would be interested in exploring multi-agent architectures and iterative self-correction for RAG systems. For example, one agent could retrieve supporting evidence, another could verify whether the generated answer is grounded in that evidence, and a third could decide whether additional retrieval or revision is necessary. I would also like to experiment with retrieval reranking and claim-level verification to identify unsupported statements more precisely. These approaches could help us better understand the tradeoff between answer quality, system complexity, and inference latency.
