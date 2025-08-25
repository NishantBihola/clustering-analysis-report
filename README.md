# Unsupervised Machine Learning: Clustering Analysis

**Author:** Nishant Bihola  
**Course:** Unsupervised ML (Booster Mode)  
**Repo:** `clustering-analysis-report`

## Executive Summary

Clustering groups similar items without labels so we can discover structure (segments, communities, topics) in data. It’s widely used in marketing, computer vision, anomaly detection, biology, social networks, and more. This report summarizes:
- What clustering is and common methods,
- 10 practical K-Means use cases,
- When/why to use Hierarchical Clustering (plus pros/cons),
- How clustering applies to social networks (community detection/influence).

## What is Clustering (in Data Mining)?

Clustering is an **unsupervised** technique that groups data points so those in the same cluster are more similar to each other than to those in other clusters. Typical workflows choose a similarity measure (e.g., Euclidean, cosine), a method (e.g., K-Means, Hierarchical, DBSCAN), and a target number of clusters (if required). Applications include customer and image segmentation, text/topic grouping, anomaly detection, and recommender systems. :contentReference[oaicite:0]{index=0}

### Common Clustering Families
- **K-Means** (partitioning): fast, needs `k`, works best with spherical clusters in numeric spaces. :contentReference[oaicite:1]{index=1}  
- **Hierarchical**: builds a dendrogram (agglomerative or divisive), no `k` required up front; you can “cut” the tree at any level. :contentReference[oaicite:2]{index=2}  
- **Density-based (DBSCAN)**: finds arbitrarily shaped clusters and marks sparse points as noise. :contentReference[oaicite:3]{index=3}  

---

## 10 Interesting Use-Cases for **K-Means**

A great, practical list of where K-Means shines includes: customer segmentation, document clustering, image compression/segmentation, anomaly/outlier detection, market basket patterns, social network grouping, delivery/dispatch zoning, IoT sensor grouping, facility placement, and color quantization (palette reduction). (Summarized from DZone’s “10 interesting use cases for the K-Means algorithm”.) :contentReference[oaicite:4]{index=4}

**Why K-Means here?** It’s simple, scalable, and fast for large numeric datasets, making it a strong default baseline for partitioning tasks. :contentReference[oaicite:5]{index=5}

---

## **Hierarchical Clustering**: Applications, Advantages, Disadvantages

**Applications.** Useful when you want a **taxonomy** or nested grouping (e.g., document/topic trees, gene expression similarities, product categorization) and when you don’t want to pre-set `k`. :contentReference[oaicite:6]{index=6}

**Advantages.**  
- Dendrogram gives **multi-resolution** views of clusters.  
- No need to specify `k` in advance.  
- Works with various linkage criteria (single/complete/average/ward). :contentReference[oaicite:7]{index=7}

**Disadvantages.**  
- Typically **more computationally expensive** than K-Means.  
- Sensitive to linkage choice and distance measure.  
- Hard to “fix” early bad merges/splits. :contentReference[oaicite:8]{index=8}

---

## Clustering in **Social Networks**

**Social Network Analysis (SNA)** represents users/organizations as **nodes** and their relationships as **edges**. Clustering (a.k.a. community detection) helps uncover subgroups, influential nodes (via centrality), and information pathways—useful for moderation, marketing, epidemiology, and misinformation research. The typical flow: build a graph, analyze centralities & communities, visualize, interpret limitations. :contentReference[oaicite:9]{index=9}

---

## Choosing Between K-Means and Hierarchical

| Scenario | Prefer K-Means | Prefer Hierarchical |
|---|---|---|
| Need speed & scale on numeric data | ✅ | — |
| Don’t know `k` & want a dendrogram | — | ✅ |
| Clusters roughly spherical/compact | ✅ | — |
| Need multi-level taxonomy | — | ✅ |
| Highly non-spherical shapes | Consider DBSCAN | Consider graph methods |

(Concepts summarized from the sources above.) :contentReference[oaicite:10]{index=10}

---

## Evaluating Clusters (quick note)

Common internal metrics: **Silhouette score**, **Davies–Bouldin index**, **Dunn index**. Silhouette (−1 to 1) balances cohesion vs. separation and is often used while tuning `k`. 

---

## References

1) *10 Interesting Use Cases for the K-Means Algorithm* — DZone. :contentReference[oaicite:12]{index=12}  
2) *Hierarchical Clustering: Applications, Advantages, and Disadvantages* — CodingInfinite. :contentReference[oaicite:13]{index=13}  
3) *What is Clustering in Data Mining?* — Scaler Topics (overview of techniques & applications). :contentReference[oaicite:14]{index=14}  
4) *Social Network Analysis (Clustering Series)* — Medium (Data Overload): nodes/edges, centrality, community detection, workflow. :contentReference[oaicite:15]{index=15}
