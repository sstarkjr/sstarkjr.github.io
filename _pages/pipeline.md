---
layout: single
title: "In the Pipeline"
permalink: /pipeline/
author_profile: true
---

Posts and projects I'm actively thinking about or planning to write up. No guarantees on timing, but this is what's on my radar.

---

## Generative AI & LLMs

**Document Intelligence Pipeline: Executive Compensation from SEC Proxy Filings**
Building a structured extraction pipeline on top of public SEC DEF 14A proxy filings using schema-enforced LLM outputs. The goal: input a ticker, get back the top 5 highest-paid executives, their full compensation mix (base, bonus, equity, other), and annualized total. Proxy filings are long, messy, and inconsistently formatted — a real test of document intelligence at scale. Draws on my background in executive compensation consulting at Mercer.

**LLM Reliability: Confidence Scores and Output Evaluation**
How do you actually know if your LLM pipeline is working well? Covers two related problems: attaching confidence scores to individual outputs (inspired by Spotify Engineering's approach), and building systematic evaluation frameworks — evals, regression testing, and production monitoring. Moving beyond vibes-based assessment toward something measurable.

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

## Strategy & Geospatial Analysis

**Retail Expansion Intelligence: TAM Estimation & Competitive Lead Generation**
A two-part project using publicly available location data to drive wholesale retail strategy. Part one: estimate total addressable market (TAM) for a product category by counting and mapping retail doors — identifying underpenetrated geographies and sizing the opportunity. Part two: reverse-engineer the Locally API (the backend powering most brand "find a retailer" pages) to systematically pull authorized retailer locations for competing brands across North America, map the overlap using Folium or Leaflet, and surface a prioritized lead list of retailers that carry competitors but not your brand. Built entirely in Python.

---

## Data Engineering & Tools

**PySpark MLlib: Predictive Modeling at Scale**
A follow-up to my earlier PySpark exploration — applying MLlib for classification or regression on large datasets, and comparing the experience to scikit-learn.

**Building Data Pipelines That Don't Break**
Lessons from production: idempotency, schema validation, monitoring, and the boring stuff that actually keeps pipelines running.
