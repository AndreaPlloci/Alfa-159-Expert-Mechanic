# Alfa 159 Technical Support Agent - AI Mechanic 🚗

This repository features a specialized AI agent designed to assist with technical troubleshooting and workshop procedures for the Alfa Romeo 159 platform.



## 🏗️ System Architecture
The agent operates through a multi-stage RAG (Retrieval-Augmented Generation) pipeline:
1. **Data Ingestion:** Technical workshop manuals are processed, partitioned using a Recursive Character Text Splitter (1000-character chunks), and stored in a Pinecone vector database.
2. **User Interface:** A Telegram Bot acts as the primary interface, receiving natural language queries from the user.
3. **Retrieval & Context:** The system performs a semantic search on the Pinecone index `alfa-romeo-expert` to retrieve the most relevant technical procedures or torque values.
4. **Augmentation:** The AI (GPT-4o) synthesizes the retrieved technical context into a precise, professional response.

## 🤖 Key Features
* **Technical Precision:** Specifically tuned to provide torque values, fluid capacities, and step-by-step mechanical procedures.
* **Context Awareness:** Utilizes a Window-Buffer-Memory (10 interactions) to maintain the thread of technical conversations.
* **Vertical RAG:** Specialized namespace management in Pinecone to ensure data purity for the Alfa 159 platform.

## 🛠️ Workflows (n8n)
* `Alfa 159 telegram.json`: Manages the Telegram webhook, AI agent logic, and user memory.
* `Upload Data Alfa 159.json`: Handles the PDF ingestion, text splitting, and vector embedding process.

---
*This project demonstrates expertise in vertical AI implementations and technical data orchestration.*
