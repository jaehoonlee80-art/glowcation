# 글로우케이션 + 슬립케이션 — 1차 MVP 확장 시안

피부 관리(글로우케이션) · 숙면(슬립케이션) · 도심 K-스파(K-스파케이션) 세 테마를
회복 목적 기준으로 묶어 검증된 회복 숙소까지 한 동선으로 보여주는 정적 프로토타입입니다.
`index.html` + `assets/img/` 실사 이미지로 동작하며(외부 라이브러리 없음) 그대로 GitHub Pages에 올라갑니다.

- 공개 주소: https://jaehoonlee80-art.github.io/glowcation/
- 호스팅: GitHub Pages (branch: `gh-pages`, `/` 루트)

## 이미지

`assets/img/` — 실사 에디토리얼 톤으로 생성한 웹 최적화 JPEG (16:10, 카드·모달 공용)

| 파일 | 쓰임 |
| --- | --- |
| `hero-performance.jpg` (1600×1000) | 히어로 문제해결 퍼포먼스 비주얼 |
| `md-01.jpg` … `sp-02.jpg` (1000×625, 12장) | 코스 카드 상단 + 상세 모달 상단 |

코스 이미지는 파일명이 코스 id와 1:1로 대응합니다(`assets/img/{id}.jpg`).
카드 상단 4장은 즉시 로드, 나머지는 `loading="lazy"`입니다.

## 수정할 때

`index.html`을 고친 뒤 **`main`과 `gh-pages` 두 브랜치 모두에 푸시**해야 사이트에 반영됩니다.
(현재 Pages 게시 소스가 `gh-pages` 브랜치로 설정되어 있습니다.)

    git add index.html assets/img README.md
    git commit -m "..."
    git push origin main
    git push origin main:gh-pages

GitHub 저장소 Settings → Pages 에서 Source를 `main` / `/ (root)`로 바꾸면
`gh-pages` 브랜치는 지워도 되고, 그때부터는 `main` 푸시만으로 배포됩니다.
