# cornell-movie-dialogue-tfidf-chatbot
"A custom TF-IDF and Cosine Similarity dialogue retrieval chatbot built from scratch in Python using the Cornell Movie-Dialogs Corpus."


# 🎬 Cornell Movie-Dialogs TF-IDF Retrieval Chatbot

An end-to-end information retrieval dialogue chatbot built from scratch using **Python**, **Pandas**, **NumPy**, and **Regex**. It processes the famous **Cornell Movie-Dialogs Corpus** to parse multi-turn dialogue pairs and uses custom-built **TF-IDF Vectorization** and **Cosine Similarity** to match incoming user queries with movie responses.

---

## 📌 Project Overview & Pipeline

1. **Dialogue Parsing:**
   * Reads raw dialogue entries from `movie_lines.tsv` and maps dialogue IDs (`line_id` ➔ `text`).
   * Extracts conversational turns from `movie_conversations.tsv` to construct $(Input_{t}, Response_{t+1})$ conversational pairs.
2. **Text Normalization:** Cleans dialogue pairs using Regular Expressions (`re`) by lowercasing text and removing special characters.
3. **Vocabulary & Custom TF-IDF Engine:**
   * Dynamically constructs the corpus vocabulary from inputs and responses.
   * Calculates **Term Frequency (TF)** normalized by sentence length.
   * Calculates **Inverse Document Frequency (IDF)** with smoothing ($\log(\frac{N + 1}{\text{count} + 1}) + 1$).
4. **Vector Similarity & Inference:**
   * Computes **Cosine Similarity** between the user's vectorized input query and stored training inputs.
   * Retrieves and outputs the dialogue response with the highest vector alignment score.

---

## 🧰 Tech Stack

* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Text Processing:** Python `re` (Regular Expressions)
* **Dataset:** Cornell Movie-Dialogs Corpus

---
