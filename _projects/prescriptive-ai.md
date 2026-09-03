---
layout: page
title: 최적의 추천 값을 제안하는 자동화된 Prescriptive AI
description: Surrogate Model과 유전 알고리즘 기반 Search Model을 결합해 목표값 달성을 위한 입력값 탐색을 자동화
importance: 6
category: 부스트캠프
---

**부스트캠프 AI Tech 7기, 2024.08 – 2025.02, 6명**

## 문제 정의

Tabular Data에서 목표값 Y를 달성하기 위한 입력값 X의 탐색을 자동화한 프로젝트입니다. X로부터 Y를 예측하는 **Surrogate Model**과, Surrogate Model을 기준으로 후보 X를 탐색하는 **Search Model**을 결합했습니다.

## 평가 지표 설계

Search Model이 여러 후보 중 정답에 가까운 X를 탐색하는지를 평가하기 위해 별도의 지표를 설계했습니다. 탐색된 후보 중 Test Data의 X와 가장 가까운 후보의 거리를 측정하고, Train Data의 평균 X와 Test Data X 사이의 거리를 기준값으로 사용해 탐색 결과를 정규화했습니다.

## 담당 역할

유전 알고리즘으로 Search Model을 구현했으며, 목표값에 대응하는 후보해를 탐색하는 문제를 구체화하고 후보해의 품질을 측정할 평가 기준을 정의했습니다.
