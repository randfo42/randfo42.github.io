---
layout: page
title: Hand Bone Image Segmentation
description: Crop 단위 학습과 Gradient Checkpointing으로 고해상도 손뼈 X-Ray 분할 성능을 Dice Score 0.66%p 개선
importance: 7
category: 부스트캠프
---

**부스트캠프 AI Tech 7기, 2024.08 – 2025.02, 6명, 팀장**

## 문제 정의

X-Ray 이미지에서 손뼈 영역의 픽셀을 클래스별로 분류하는 Multi-Label Segmentation 프로젝트입니다. 팀장으로서 성능 개선 가설을 수립하고, 팀이 공통으로 사용할 Baseline 코드와 실험 환경을 구성했습니다.

## 접근 방법

원본 이미지의 해상도가 높아 학습 과정에서 이미지를 축소하면 손뼈의 세부 정보가 손실될 수 있다고 판단했습니다. 이에 이미지를 축소하는 대신 **Crop 단위**로 학습해 4개 클래스의 평균 **Dice Score를 0.66%p 향상**했습니다. 또한 **Gradient Checkpointing**을 적용해 제한된 GPU 메모리에서 더 높은 해상도의 이미지를 학습할 수 있도록 구성했습니다.

## 담당 역할

**MMSegmentation**을 Multi-Label Task에 맞게 수정했으며, 수립한 가설과 Baseline 코드를 팀에 공유해 이를 중심으로 실험을 진행했습니다.
