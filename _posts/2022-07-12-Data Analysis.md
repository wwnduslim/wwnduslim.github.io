---
layout: post
title: Data Analysis (Big Data)
date: 2022-07-12 14:00 +0800
last_modified_at: 2022-07-12 13:00 +0800
tags: [코딩테스트, 프로그래머스]
toc:  true
layout: archive-taxonomies
type: categories
---

# Data Analysis

## Dacon

## 1. Credit Card Fraud Detection
### Introduction
- In this kernel I will use various predictive models to see how accurate they are in detecting whether a transaction is a normal payment or a fraud. As described in the dataset, the features are scaled and the names of the features are not shown due to privacy reasons. Nevertheless, we can still analyze some important aspects of the dataset. Let's start!

### Datasets
- You can download the datasets from kaggle(Credit Card Fraud Detection). These datasets are the actual transaction record of credit card users in Europe in September 2013, and a total of 284,807 transaction details are provided. Of these, 492 cases were fraudulent transactions, and fraudulent transactions were characterized by a very small proportion compared to normal transactions. That's why we call it a 'Highly unbalanced' dataset.

### My goals
- Totally understand the little distribution of the data that was provided.
- Determine the Classifiers we are going to use and decide which one has a higher accuracy.
- Understand common mistake made with imbalanced datasets and be able to correct it by myself.