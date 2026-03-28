---
layout: single
title: "In the Pipeline"
permalink: /pipeline/
author_profile: true
---

Posts and projects I'm actively thinking about or planning to write up. No guarantees on timing, but this is what's on my radar.

---

## Generative AI & LLMs

**Confidence Scores for GenAI Applications**
Inspired by Spotify Engineering's approach to attaching reliability signals to LLM outputs. Want to apply similar techniques to my own datasets and document what works in practice.

**Document Intelligence Pipeline**
Building a structured extraction pipeline on top of public documents — likely SEC filings or patent applications — using schema-enforced LLM outputs. A natural extension of the RAG work I've done, but focused on producing clean, queryable structured data rather than free-form answers.

**LLM Output Evaluation in Practice**
How do you actually know if your LLM pipeline is working well? Moving beyond vibes-based evaluation toward systematic approaches: evals, regression testing, and monitoring in production.

---

## NLP & Text Analysis

**Social Sentiment Monitoring Pipeline**
End-to-end walkthrough of collecting social data (Reddit/other), running sentiment analysis, clustering topics, and visualizing trends over time. A practical guide to building a brand or topic listening system from scratch.

**When Topic Modeling Goes Wrong**
A more honest look at failure modes in embedding-based topic modeling — when HDBSCAN produces noise-heavy results, when TF-IDF labels mislead, and how to diagnose and fix it.

---

## Machine Learning

**Anomaly Detection on Behavioral Data**
Applying unsupervised anomaly detection (Isolation Forest, DBSCAN, AutoEncoders) to publicly available behavioral or performance data. Interested in the intersection of clustering and anomaly flagging — where something is *unusual* vs. just *different*.

**Practical A/B Testing**
Moving beyond the basics — sequential testing, stopping rules, and how to run experiments when you can't wait for a perfectly powered sample size.

---

## Data Engineering & Tools

**PySpark MLlib: Predictive Modeling at Scale**
A follow-up to my earlier PySpark exploration — applying MLlib for classification or regression on large datasets, and comparing the experience to scikit-learn.

**Building Data Pipelines That Don't Break**
Lessons from production: idempotency, schema validation, monitoring, and the boring stuff that actually keeps pipelines running.
