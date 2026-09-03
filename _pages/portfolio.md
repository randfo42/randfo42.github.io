---
layout: page
title: Portfolio
permalink: /portfolio/
description: 3D Bin Packing, MLOps 파이프라인, 얼굴인식 연구를 정리한 포트폴리오입니다.
nav: true
nav_order: 6
---

<style>
  .pdf-embed {
    margin-bottom: 1rem;
  }

  /*
    원본은 1440x810(16:9) 가로형 덱이다. 다만 16/9로 딱 맞추면 브라우저 PDF
    뷰어의 툴바(약 48px)가 그 안을 차지해 슬라이드 아래가 잘린다.
    뷰포트 높이 기준으로 여유를 두고 잡는다.
  */
  .pdf-embed object {
    width: 100%;
    height: 78vh;
    min-height: 420px;
    border: 1px solid var(--global-divider-color);
  }

  /*
    iOS Safari와 안드로이드 Chrome은 object/iframe 안의 PDF를 인라인으로
    렌더하지 않고 첫 페이지만 정지 이미지처럼 보여주거나 빈 칸을 남긴다.
    좁은 화면에서는 뷰어를 감추고 아래 링크만 남긴다.
  */
  @media (max-width: 575.98px) {
    .pdf-embed {
      display: none;
    }
  }

  .pdf-fallback {
    font-size: 0.9rem;
  }
</style>

<div class="pdf-embed">
  <object data="{{ '/assets/pdf/portfolio.pdf' | relative_url }}" type="application/pdf">
    <p>이 브라우저에서는 PDF를 페이지 안에 표시할 수 없습니다. 아래 링크로 열어 주세요.</p>
  </object>
</div>

<p class="pdf-fallback">
  PDF가 보이지 않으면
  <a href="{{ '/assets/pdf/portfolio.pdf' | relative_url }}" target="_blank" rel="noopener">새 탭에서 열기</a>
  (13페이지, 2.5MB)
</p>
