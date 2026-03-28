---
layout: single
title: "Reading List"
permalink: /reading-list/
author_profile: true
---

A running list of articles, papers, and resources I've found worth reading. Grouped loosely by topic.

---

## Generative AI & LLMs

- **[Building Confidence: A Case Study in How to Create Confidence Scores for GenAI Applications](https://engineering.atspotify.com/2024/12/building-confidence-a-case-study-in-how-to-create-confidence-scores-for-genai-applications)** — Spotify Engineering
  Practical approach to attaching reliability signals to LLM outputs in production. Useful for anyone moving GenAI beyond the demo stage.

- **[7 Mistakes People Make When Trying to Become an AI Engineer](https://www.youtube.com/watch?v=nvc7xi6vZWw)** — YouTube
  Common pitfalls when breaking into AI engineering — why grinding through courses often stalls progress and what to do instead.

- **[Patterns for Building LLM-based Systems & Products](#)** — Eugene Yan
  One of the best practical overviews of LLM system design — evals, retrieval, agents, and more. Reference-level writing.

- **[Prompt Engineering Guide](#)** — DAIR.AI
  Comprehensive and regularly updated. Good for both fundamentals and advanced techniques like chain-of-thought and self-consistency.

---

## Embeddings & Vector Search

- **[The Illustrated Word2Vec](#)** — Jay Alammar
  The clearest visual explanation of how word embeddings work. Jay Alammar's blog is consistently excellent.

- **[Not All Vector Databases Are Made Equal](#)** — Dmitry Kan
  Practical comparison of vector DB options (Pinecone, Weaviate, Qdrant, etc.) with real benchmarks.

- **[Text Embeddings Reveal (Almost) As Much As Text](#)** — arXiv
  Interesting research on how much information is recoverable from embeddings — relevant for privacy and security thinking.

---

## NLP & Topic Modeling

- **[Unlocking Insights from Qualitative Text with LLM-Enhanced Topic Modeling](https://www.amazon.science/blog/unlocking-insights-from-qualitative-text-with-llm-enhanced-topic-modeling)** — Amazon Science
  Amazon's approach to combining LLMs with topic modeling for qualitative text analysis. Closely related to the embedding + clustering pipeline I've used on customer review data.

- **[BERTopic: Neural topic modeling with BERT](#)** — Maarten Grootendorst
  The paper behind a library I use regularly. Explains the UMAP + HDBSCAN + class-based TF-IDF pipeline clearly.

- **[Topic Modeling in Embedding Spaces](#)** — arXiv
  Good theoretical grounding for why embedding-based topic models outperform LDA on short texts.

---

## Data Science & ML in Practice

- **[Rules of Machine Learning: Best Practices for ML Engineering](#)** — Martin Zinkevich, Google
  43 rules drawn from production ML experience at Google. More useful than most textbooks.

- **[Tidy Data](#)** — Hadley Wickham
  Old but timeless. The principles here inform how I think about data modeling regardless of language or tool.

- **[The Unreasonable Effectiveness of Data](#)** — Alon Halevy, Peter Norvig, Fernando Pereira
  Makes the case for scale over cleverness. Relevant context whenever someone argues about model architecture vs. data quality.

---

## Engineering & Tooling

- **[Designing Data-Intensive Applications (excerpts)](#)** — Martin Kleppmann
  The chapters on distributed systems fundamentals are required reading for anyone building pipelines at scale.

- **[Stop Using datetime.now()](#)** — Various
  A recurring lesson: time handling in data pipelines is much harder than it looks. Good reminder to be explicit about timezones everywhere.

---

## Strategy & Thinking

- **[The Bitter Lesson](#)** — Rich Sutton
  Short, provocative essay arguing that general methods leveraging computation consistently beat human-knowledge-heavy approaches. Worth revisiting periodically.

- **[Maker's Schedule, Manager's Schedule](#)** — Paul Graham
  Classic framing for why context-switching is so costly for technical work. Useful for setting expectations with stakeholders.
