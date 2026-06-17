# Portfolio · Five Keywords

입사지원용 포트폴리오 정적 웹사이트입니다. 원본 HTML의 내용과 흑백 편집형 디자인을 유지하면서, GitHub Pages에 바로 올릴 수 있는 구조로 정리했습니다.

## 구성

- `index.html`: 실제 포트폴리오 페이지입니다. 내용과 디자인을 수정할 때 이 파일을 편집하면 됩니다.
- `.github/workflows/deploy-pages.yml`: `main` 브랜치에 푸시되면 GitHub Pages로 자동 배포하는 워크플로입니다.
- `.nojekyll`: GitHub Pages가 Jekyll 빌드를 시도하지 않도록 막습니다.
- `robots.txt`: 검색엔진 접근 허용 파일입니다.

## 추천 배포 방식

현재 사이트는 서버 기능이 필요 없는 정적 사이트라서 GitHub Pages가 가장 단순하고 안정적인 선택입니다.

목표 배포 주소:

```text
https://kanto00.github.io/iyehyoung/
```

1. GitHub에서 `kanto00/iyehyoung` public 저장소를 만듭니다.
2. 이 폴더 안의 파일들을 저장소 루트에 올립니다.
3. 저장소 `Settings` → `Pages`로 이동합니다.
4. `Build and deployment`의 `Source`를 `GitHub Actions`로 설정합니다.
5. `main` 브랜치에 푸시하면 Actions가 실행되고, 완료 후 Pages URL이 생성됩니다.

Git으로 올릴 때는 저장소 생성 후 아래 명령을 사용합니다.

```bash
git remote add origin https://github.com/kanto00/iyehyoung.git
git push -u origin main
```

## 로컬 확인

파일을 바로 열어도 동작합니다.

```bash
open index.html
```

또는 간단한 로컬 서버로 확인할 수 있습니다.

```bash
python3 -m http.server 4173
```

이후 브라우저에서 `http://localhost:4173`을 열면 됩니다.

## 나중에 하면 좋은 것

- 이름, 연락처, 지원 직무, 대표 프로젝트 링크를 상단에 추가
- 실제 배포 URL이 생긴 뒤 `og:url` 메타 태그 추가
- 개인 도메인을 쓸 경우 GitHub Pages의 Custom domain 설정 추가
