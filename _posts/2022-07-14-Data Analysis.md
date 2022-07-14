---
layout: post
title: Data Analysis
date: 2022-07-14 13:56 +0800
last_modified_at: 2022-07-14 13:56 +0800
tags: [데이터분석, Data]
toc:  true
---

# Various Models

## Supervised / Unsupervised Models

### Introduction
- In this kernel I will deal with various models on data analysis. By using various predictive models, I will see how accurate they are in detecting train / test datas. 
- By learning in details, I hope I will be able to analyze some important aspects of the dataset. Let's start!

## 1. Unsupervised Models
- Clustering
    - Clustering is one of the machine-learning methods that classify the datas by the similar characteristics. It us commonly used in pattern recognition or sorting the similar news. KMeans, DBSCAN, Hierachical clustering, Spectral Clustering are the examples of Clustering algorithm. 

    image.png


    비슷한 뉴스나 사용 패턴이 유사한 사용자를 묶어 주는것과 같은 패턴 인지나, 데이타 압축등에 널리 사용되는 학습 방법이다.클러스터링은 라벨링 되어 있지 않은 데이타를 묶는 경우가 일반적이기 때문에 비지도학습 (Unsupervised learning) 학습 방법이 사용된다.클러스터링 알고리즘은 KMeans, DBSCAN, Hierarchical clustering, Spectral Clustering 등 여러가지 기법이 있으며, 알고르즘의 특성에 따라 속도나 클러스터링 성능에 차이가 있기 때문에, 데이타의 모양에 따라서 적절한 클러스터링 알고리즘을 선택하는 것이 중요하다. 다음은 sklearn에 나와 있는 각 클러스터링 알고리즘의 성능에 대한 비교표이다. 