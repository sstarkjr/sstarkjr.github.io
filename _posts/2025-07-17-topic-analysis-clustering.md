---
title: "Discovering Topics in Text with Clustering and Embeddings"
date: 2025-07-17
permalink: /posts/2025/07/topic-analysis-clustering/
tags:
  - NLP
  - embeddings
  - text clustering
  - topic modeling
  - unsupervised learning
---
## My End-to-End Workflow for Topic Discovery

When I wanted to surface themes from customer reviews, I knew I needed something more powerful than word clouds or manual tagging. I ended up building a pipeline that combines large language models, semantic embeddings, clustering, and a bit of TF-IDF magic.

Here’s the overall process I used:

### 1. Start with Raw Reviews

We'll start with a hotel reviews dataset. We don't know much about the hotels, the reviewers, or time period. But, we know the dataset is full reviews from real customers. These are messy, informal, and vary widely in length and content.

### 2. Use an LLM to Extract Key Phrases

Instead of clustering entire reviews (which often contain multiple unrelated ideas), I use a language model to extract **key phrases** from each review. These phrases act as concise summaries of the main points. Each review often has one or more key phrases.

### 3. Deduplicate and Explode

Once I’ve got key phrases:

* I **deduplicate** overlapping phrases.
* Then I **explode** the data so that each row contains a single key phrase. This step flattens the structure for easier downstream processing.

### 4. Generate Embeddings

Each key phrase is embedded using a sentence transformer like OpenAI's `text-embedding-3-small`. This converts the text into a high-dimensional vector that captures its semantic meaning.

### 5. Reduce Dimensions for Visualization

I use **UMAP** to reduce these embeddings to 2D so I can visualize them. This helps reveal natural groupings or clusters in the data.

### 6. Cluster the Embeddings

With the reduced vectors, I apply the **HDBSCAN** clustering algorithm to group similar key phrases. Each cluster tends to represent a recurring topic or theme.

### 7. Profile Each Cluster

To understand what each cluster is about, I analyze:

* **TF-IDF scores** to find distinctive terms
* **Word frequency** to highlight the most common phrases

This gives me a way to label clusters with topics like “ambiance,” “pillows,” or “location”. This list of topics is the beginning of a taxonomy of which can be used to identify topic and sentiment in a set of reviews.

---
## 🔍 From Raw Review to Key Phrases

Let’s walk through a concrete example of how a review gets transformed in this process.

### Original Review:

> “We stayed here for two nights. The location was perfect — walking distance to everything! Staff were friendly, but the pillows were way too soft. Also, we could hear everything through the walls.”

This review contains multiple themes: location, service, sleep comfort, and noise complaints. Clustering this entire paragraph as a single unit would muddle those signals.

### LLM-Extracted Key Phrases:

Using a language model, we break it into bite-sized, theme-specific phrases:

* *great location*
* *friendly staff*
* *pillows too soft*
* *noisy rooms*

These are the atomic units that go into the clustering step — short, specific, and semantically rich.

> *LLMs don’t just summarize — they distill the review into a list of things the person cared about, which is much more useful when you're trying to surface patterns.*

---

## 🎨 What the Clusters Look Like

Once each phrase is embedded and plotted with UMAP, clusters start to emerge. Here’s a snapshot of what I saw in my hotel reviews data:

* Cluster 2: *“thin walls”, “noisy at night”, “hear neighbors”*
* Cluster 4: *“perfect location”, “near metro”, “close to shops”*
* Cluster 7: *“comfy bed”, “hard pillows”, “pillows too flat”*

Each group represents a theme that shows up across dozens or hundreds of reviews — even if the original phrasing was different.

> One of my favorite surprises: a cluster filled with phrases like “free upgrade,” “bottle of champagne,” and “anniversary surprise.” That’s not something you'd find with basic keyword search — it took the LLM to understand the deeper sentiment.

---

## 📊 Clusters, Counted and Profiled

To help label the clusters, I calculate:

* How many phrases are in each one (cluster size)
* Which words appear most often (frequency)
* Which are the most distinctive (TF-IDF)

Here’s what that looks like in practice:

| Cluster | Size | Top Phrases                                   |
| ------- | ---- | --------------------------------------------- |
| 0       | 148  | thin walls, loud neighbors, hallway noise     |
| 1       | 96   | friendly staff, helpful front desk, welcoming |
| 2       | 203  | great location, near metro, walkable area     |

This gives you a fast, explainable way to name each group — and can even be used to create dashboard labels or drive product insights.

---

## 💡 Why This Approach Works

Traditional topic modeling (like LDA) often struggles with nuance, phrasing variation, or short texts. This embedding-based method solves that by:

* Capturing **semantic meaning** (not just word overlap)
* Handling **short phrases** gracefully
* Letting LLMs do the heavy lifting on phrase extraction

Together, the result is more **interpretable**, **scalable**, and **practical** for use cases like:

* Tagging reviews
* Building taxonomies
* Tracking customer themes over time

---
