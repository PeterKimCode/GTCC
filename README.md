# myyoungji_new (General Trias College of Cavite Website)

General Trias College of Cavite (GTCC)의 공식 웹사이트 소스 코드입니다. 이 프로젝트는 정적(Static) 웹사이트로 구축되었습니다.

## 🛠 기술 스택 (Tech Stack)
- **HTML5**: 웹 페이지 구조 정의
- **Tailwind CSS (CDN)**: 스타일링 및 반응형 디자인 (`<script src="https://cdn.tailwindcss.com"></script>` 사용)
- **Vanilla JavaScript**: 동적 기능 및 로직 구현 (외부 라이브러리 의존성 최소화)

## 📂 데이터 저장 위치 (Data Storage)
이 웹사이트는 별도의 백엔드 데이터베이스(DB)를 사용하지 않습니다. 모든 데이터는 클라이언트 측 코드에 포함되어 있습니다.

1.  **웹사이트 콘텐츠 (텍스트/이미지)**:
    *   각 HTML 파일(`index.html`, `admission/index.html` 등)에 직접 하드코딩되어 있습니다.
2.  **네비게이션 메뉴 구조**:
    *   `assets/js/main.js` 파일 내의 `NAV` 상수 배열에 정의되어 있습니다. 메뉴 변경 시 이 배열을 수정하면 사이트 전체에 반영됩니다.
3.  **학생 검색 데이터 (Student Search)**:
    *   `assets/js/main.js` 파일 내의 `STUDENT_RECORDS` 배열에 JSON 형태의 객체로 저장되어 있습니다.
    *   이곳에 학생 정보를 추가하거나 수정하면 검색 기능에 자동 반영됩니다.

## ✨ 주요 기능 (Key Features)

1.  **동적 네비게이션 생성 (Dynamic Navigation)**
    *   `NAV` 배열을 기반으로 상단 메뉴(Top Nav), 사이드바(Sidebar), 모바일 메뉴(Mobile Nav), 브레드크럼(Breadcrumbs)을 자동으로 생성합니다.
    *   페이지 깊이(Depth)에 따라 경로를 자동으로 계산합니다.

2.  **반응형 디자인 (Responsive Design)**
    *   모바일 환경을 완벽하게 지원하며, 햄버거 메뉴 및 모바일 전용 UI가 구현되어 있습니다.

3.  **학생 검색 기능 (Student Search)**
    *   `/community/search-for-student/` 페이지에서 학번 등으로 학생을 검색할 수 있습니다.
    *   데이터는 `assets/js/main.js`의 `STUDENT_RECORDS`에서 실시간으로 필터링됩니다.

4.  **히어로 슬라이더 (Hero Slider)**
    *   메인 페이지의 이미지 슬라이더는 외부 플러그인 없이 자체 구현되었으며, 자동 재생 및 터치/키보드 탐색을 지원합니다.

5.  **다국어 지원 (Google Translate)**
    *   Google Translate 위젯을 통합하여 다국어 번역을 지원합니다.

## 📁 프로젝트 구조 (Project Structure)
```
myyoungji_new/
├── assets/             # JavaScript, CSS 등 공용 리소스
│   └── js/main.js      # 핵심 로직 및 데이터 (NAV, STUDENT_RECORDS)
├── images/             # 이미지 파일
├── admission/          # 입학 관련 페이지
├── basic-education/    # 교육 과정 관련 페이지
├── community/          # 커뮤니티 및 뉴스 페이지
├── e-education/        # e-러닝 관련 페이지
├── youngji_about-us/   # 학교 소개 페이지
├── partials/           # 헤더, 푸터 등 HTML 조각 (fetch로 로딩)
└── index.html          # 메인 홈페이지
```

## 🚀 실행 방법 (How to Run)
이 프로젝트는 정적 사이트이므로 별도의 빌드 과정이 필요 없습니다.
1.  프로젝트 폴더를 엽니다.
2.  `index.html` 파일을 브라우저로 열거나, VS Code의 `Live Server` 확장을 사용하여 실행합니다.