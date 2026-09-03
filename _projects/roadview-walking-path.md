---
layout: page
title: 로드뷰를 활용한 산책로 찾기
description: 저사양 GPU에서 vLLM으로 VLM을 서빙하며 병목을 분석해 처리량을 2.85배 개선
importance: 5
category: 개인 프로젝트
---

**개인 프로젝트, 2026.08**

## 문제 정의

로드뷰를 활용하여 산책로를 찾는 프로젝트입니다. GTX 1660 6GB에서 **vLLM**을 통해 **Gemma4 E2B**를 서빙하고, VLM 모델의 병목을 파악해 처리량을 2.85배 늘렸습니다.

## 접근 방법

Gemma4 E2B는 VRAM 6GB에 들어가지 않았기에, PLE embedding table을 CPU memory로 옮기고 GPU가 메모리 주소를 참조할 수 있도록 **UVA view**를 적용했습니다. Embedding table의 경우 row select로 구현되어 있어 해당 layer만 따로 처리할 수 있었습니다.

또한 decode보다 prefill intensive한 task이고 적은 토큰의 prompt를 공유하는 프로젝트였기에, **KV cache**보다 병렬처리를 신경 쓰며 vLLM을 서빙했습니다.

## 결과 및 트레이드오프

- `max-num-seqs`를 1에서 32로 늘리자 처리량은 **41% 증가**했지만 linear하게 증가하는 모습은 보이지 않았습니다.
- VLM 특성상 vision encoder가 병목임을 파악했고, 이미지 토큰 크기를 줄여 precision을 **94.4%에서 92.7%로 1.7%p 희생**하는 대신 처리량을 **2.85배** 높였습니다.
