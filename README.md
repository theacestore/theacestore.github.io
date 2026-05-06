# 라벨랩(Label Lab) 웹사이트

Astro로 구축된 라벨랩(Label Lab)의 프리미엄 B2B 제조 전문 웹사이트입니다.

이 사이트는 CAB 자동 라벨링 시스템, 무봉제 웰딩 PU 로고, 정밀 다이컷 부품, 인쇄 라벨, 포장 자재 및 롤 라벨 공급을 포함하여 라벨랩을 하이엔드 산업 솔루션 파트너로 포지셔닝합니다.

## 기술 스택

- Astro
- TypeScript (Strict Mode)
- 컴포넌트 기반 UI 아키텍처
- GitHub Pages용 정적 출력(Static Output)

## 프로젝트 구조

```text
src/
  layouts/
    BaseLayout.astro     # 기본 레이아웃
  components/
    Header.astro         # 헤더
    Footer.astro         # 푸터
    Hero.astro           # 메인 히어로 섹션
    ProductBento.astro   # 제품 벤토 그리드 레이아웃
    ProductCard.astro    # 개별 제품 카드
    DetailPage.astro     # 상세 페이지 공통 컴포넌트
  pages/
    index.astro          # 메인 페이지
    details/             # 제품 상세 페이지들
      barcode-label.astro
      package-materials.astro
      poron-diecut.astro
      print-label.astro
      seamless-welding.astro
      thermal-label.astro
  styles/
    global.css           # 전역 스타일링

public/
  images/                # 정적 이미지 자산
  favicon.svg            # 파비콘
```

## 개발 방법

의존성 설치:

```bash
npm install
```

로컬 개발 서버 실행:

```bash
npm run dev
```

로컬 접속 주소:

```text
http://127.0.0.1:4321/
```

## 빌드 및 배포

```bash
# 정적 파일 빌드
npm run build
```

빌드 결과물 미리보기:

```bash
npm run preview
```

## 품질 확인 (타입 및 구문 체크)

```bash
npm exec astro check
```

## GitHub Pages 설정

Astro 설정 파일(`astro.config.mjs`)은 GitHub Pages에 맞게 준비되어 있습니다:

```js
export default defineConfig({
  site: "https://theacestore.github.io",
  output: "static",
});
```

배포 자동화:
`.github/workflows/deploy.yml` 파일에 정의된 워크플로우를 통해 진행됩니다. `main` 브랜치에 푸시하면 자동으로 GitHub Pages 배포가 시작됩니다.

## 참고 사항

- 현재 프로덕션 소스는 `src/` 및 `public/` 폴더 내에 있습니다.
- 루트 디렉토리에 있는 기존 HTML 파일들은 Astro 사이트의 주요 소스가 아닙니다.
- Astro에서 사용하는 정적 이미지 자산은 `public/images/`에 저장되어 있습니다.
