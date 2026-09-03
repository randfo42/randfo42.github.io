---
layout: about
title: 소개
permalink: /
subtitle: >
  AI Engineer, 아주대학교 인공지능학과 석사<br>
  <a href="mailto:randfo42@gmail.com">randfo42@gmail.com</a> |
  <a href="https://github.com/randfo42">github.com/randfo42</a>

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular

selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: true # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

<style>
  /*
    기본 about 레이아웃은 사진을 float-right 시키고 소개를 그 옆에 흘린다.
    소개가 짧아 사진 위쪽에만 붙고 아래로 빈 공간이 남으므로,
    article을 2열 grid로 바꿔 소개를 사진 높이의 가운데에 맞춘다.
    (모바일에서는 기존 세로 배치를 그대로 둔다.)
  */
  @media (min-width: 576px) {
    .post > article {
      display: grid;
      grid-template-columns: 1fr auto;
      column-gap: 2rem;
      align-items: center;
    }

    .post > article > * {
      grid-column: 1 / -1;
    }

    .post > article > .profile {
      grid-column: 2;
      grid-row: 1;
      float: none;
      width: 120px;
      margin-left: 0;
    }

    .post > article > .clearfix {
      grid-column: 1;
      grid-row: 1;
    }
  }

  /* news 목록은 남기고 'news' 제목만 숨긴다 (제목은 테마 gem에 하드코딩되어 있음) */
  .post > article > h2:has(> a[href$="/news/"]) {
    display: none;
  }
</style>

모호한 문제를 측정 가능한 ML 문제로 정의하고,

모델 실험부터 MLOps 구축까지 경험한 AI Engineer입니다.
