---
layout: page
title: 재활용 품목 분류를 위한 Object Detection
description: Contrastive Loss를 적용한 Detectron2로 Baseline 대비 mAP50을 3.3%p 향상
importance: 8
category: 부스트캠프
---

**부스트캠프 AI Tech 7기, 2024.08 – 2025.02, 6명, 팀장**

## 문제 정의

재활용 이미지에서 품목의 위치와 종류를 탐지하는 Object Detection 프로젝트입니다. 팀장으로서 **Detectron2**와 **MMDetection** 기반의 Baseline 코드 및 서버 환경을 구성해 팀에 공유했습니다.

## 가설 및 접근 방법

동일한 클래스 안에서도 객체의 형태가 다양하다는 점에 주목했습니다. 같은 클래스의 객체 표현을 임베딩 공간에서 가깝게 학습하면 클래스 내 형태 차이에도 일관된 특징을 학습할 수 있다고 가정했습니다.

이를 검증하기 위해 Detectron2를 수정해 **Contrastive Loss**를 적용했습니다.

## 결과

Baseline 대비 **mAP50을 3.3%p 향상**했습니다.
