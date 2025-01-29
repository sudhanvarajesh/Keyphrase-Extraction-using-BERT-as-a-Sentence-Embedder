# 🔑 Keyphrase Extraction using BERT as a Sentence Embedder  

## 📄 Overview  

Keyphrases are **words or short phrases** that best describe the content of a given text document. This project leverages **BERT (Bidirectional Encoder Representations from Transformers) as a sentence embedder** to understand the context of a given sentence more effectively.  

The approach involves computing **cosine similarity** between the **document embedding** and the **phrase embeddings** of candidate keyphrases, ranking them based on their relevance.  

## ✨ Key Features  

- **BERT-based Sentence Embeddings** for contextual understanding  
- **Cosine Similarity** to rank keyphrases  
- **Automatic Extraction** of keyphrases from text documents  
- **Optimized Ranking Algorithm** for high-quality keyphrases  

## 🏗️ Methodology  

1. **Document & Candidate Phrase Embedding:**  
   - The entire document is encoded using **BERT** to obtain its **document embedding**.  
   - Candidate keyphrases are extracted and encoded into **phrase embeddings**.  

2. **Cosine Similarity Computation:**  
   - Each phrase embedding is compared with the document embedding using **cosine similarity**.  
   - Higher similarity scores indicate more relevant keyphrases.  

3. **Keyphrase Ranking:**  
   - Candidate keyphrases are ranked in descending order based on cosine similarity scores.  
   - The **top-ranked phrases** are selected as keyphrases for the document.  

## 🛠️ Tech Stack  

- **NLP Model:** BERT (Sentence Transformer)  
- **Similarity Metric:** Cosine Similarity  
- **Libraries:**  
  - Python  
  - `transformers` (Hugging Face)  
  - `sentence-transformers`  
  - `scikit-learn`  
  - `numpy`  

## 🔧 Setup & Installation  

### 1️⃣ Clone the Repository  

```bash
git clone https://github.com/sudhanvarajesh/Keyphrase-Extraction-using-BERT-as-a-Sentence-Embedder
cd keyphrase-extraction-bert
```

### 2️⃣ Install Dependencies  

```bash
pip install -r requirements.txt
```

### 3️⃣ Run the Script  

```bash
python extract_keyphrases.py --input "sample_text.txt"
```

## 📊 Example Usage  

```python
from keyphrase_extractor import extract_keyphrases

document = "Natural Language Processing (NLP) is a branch of AI that focuses on the interaction between computers and humans using natural language."

keyphrases = extract_keyphrases(document, top_n=5)
print(keyphrases)
```

**Expected Output:**  
```bash
["Natural Language Processing", "NLP", "AI", "interaction", "natural language"]
```

## 🚀 Future Improvements  

- Experimenting with different transformer models like **RoBERTa** and **DistilBERT**  
- Improving candidate phrase extraction using dependency parsing  
- Optimizing performance for large documents  


## 👨‍💻 Contributing  

We welcome contributions! To contribute:  

1. Fork the repository  
2. Create a feature branch (`git checkout -b feature-name`)  
3. Commit your changes (`git commit -m "Added feature"`)  
4. Push to your fork (`git push origin feature-name`)  
5. Open a Pull Request  
