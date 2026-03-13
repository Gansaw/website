# HoJin Choi — Portfolio Website

비행 데이터 분석가이자 AI 엔지니어 최호진의 개인 포트폴리오 웹사이트입니다.  
항공우주 데이터 분석, 머신러닝 프로젝트, 인사이트 아티클, 수료증을 담고 있습니다.

**🌐 Live Website**: [gansaw.github.io/website](https://gansaw.github.io/website)

---

## 📁 파일 구조

```
website/
├── index.html          # 메인 페이지 (About / Skills / Career / Contact)
├── project.html        # 프로젝트 목록 및 상세 모달 (WYSIWYG 에디터 내장)
├── article.html        # 아티클 목록 및 읽기 뷰 (WYSIWYG 에디터 내장)
├── certificate.html    # 수료증 목록 및 이미지 뷰어
├── style.css           # 통합 스타일시트
├── assets/
│   └── certificates/   # 수료증 이미지 자동 업로드 경로
└── README.md           # 프로젝트 문서
```

---

## 📄 페이지 소개

### 🏠 index.html — 메인 페이지
About, Skills, Career, Contact 섹션으로 구성된 단일 페이지입니다.  
상단 네비게이션에서 Project / Article / Certificate 페이지로 직접 이동할 수 있으며, 히어로 섹션의 CTA 버튼에도 각 페이지 링크가 배치되어 있습니다.

### 🔬 project.html — 프로젝트
Statistics / Data Analysis / AI·ML 카테고리로 필터링할 수 있는 프로젝트 카드 목록입니다.  
카드 클릭 시 Problem · Solution · Results 및 Quill 에디터로 작성한 상세 설명을 모달로 확인할 수 있습니다.

### 📝 article.html — 아티클
Insight / Paper Review 카테고리의 아티클 카드 목록입니다.  
카드 클릭 또는 View Details 버튼으로 본문 읽기 뷰로 전환되며, 파일 첨부 기능도 지원합니다.

### 🎓 certificate.html — 수료증
Coursera / Udemy / Google / Microsoft / AWS / UTS / Other 플랫폼으로 필터링할 수 있는 수료증 카드 목록입니다.  
수료증 이미지를 업로드하면 GitHub `assets/certificates/` 경로에 자동 커밋되며, 썸네일 클릭 시 전체화면 이미지 뷰어가 열립니다.  
Verify 버튼으로 외부 수료증 URL(Coursera 검증 링크 등)로 바로 이동할 수 있습니다.

---

## ✨ 주요 기능

### ✍️ WYSIWYG 에디터 (project / article)
**Quill.js** 기반으로 HTML 태그 없이 글꼴·크기·굵기·목록·인용구·링크 등을 시각적으로 편집할 수 있습니다.

### 🚀 GitHub API 실시간 연동
작성·수정·삭제한 내용이 GitHub REST API를 통해 레포지토리에 직접 커밋되어 실시간으로 반영됩니다.  
수료증 이미지는 `assets/certificates/` 경로에 별도 커밋됩니다.

### 🎨 UI/UX
- 각 카드 하단에 **View Details →** / **Verify →** / **Edit** / **Delete** 버튼 배치
- 플랫폼·카테고리별 컬러 배지로 한눈에 구분 가능
- certificate 페이지 상단에 총 수료증 수·플랫폼별 통계 배너 표시
- 전체 스타일은 `style.css`에서 중앙 집중식으로 관리

---

## 🔁 GitHub 커밋 메시지 규칙

| 동작 | 커밋 메시지 |
|---|---|
| 새 항목 등록 | `✍️ Add project/article/certificate: <제목>` |
| 항목 수정 | `✏️ Edit project/article/certificate: <제목>` |
| 항목 삭제 | `🗑 Delete project/article/certificate: <제목>` |
| 이미지 업로드 | `📎 Upload certificate image: <파일명>` |

---

## ✍️ 사용법

### 🔑 GitHub Token 설정
글·수료증을 등록하거나 수정하려면 GitHub Personal Access Token이 필요합니다.

1. 각 페이지 우측 하단 **🔑** 버튼 클릭
2. [GitHub Token 발급 페이지](https://github.com/settings/tokens/new?scopes=repo&description=portfolio-write)에서 `repo` 권한 체크 후 발급
3. 발급된 토큰 입력 후 **💾 저장** 클릭
   - 토큰은 브라우저 로컬 스토리지에만 저장되며 외부로 전송되지 않습니다.
   - project / article / certificate 페이지는 각각 별도의 토큰 키로 저장됩니다.

### 📝 항목 작성 / 수정 / 삭제

| 동작 | 방법 |
|---|---|
| 새 항목 등록 | 우측 하단 **✍️** (또는 **🎓**) 버튼 클릭 |
| 항목 수정 | 카드 하단 **Edit** 버튼 클릭 |
| 항목 삭제 | 카드 하단 **Delete** 버튼 클릭 |

등록 버튼을 누르면 GitHub에 즉시 커밋되며, 약 2~3초 후 페이지가 자동으로 새로고침됩니다.

### 🖼️ 수료증 이미지 업로드 (certificate.html)
1. **🎓** FAB 버튼으로 등록 모달 열기
2. **🖼️ 이미지 선택** 버튼으로 JPG / PNG 파일 선택
3. 미리보기 확인 후 **📤 GitHub에 등록** 클릭
   - 이미지는 `assets/certificates/cert_<timestamp>.<ext>` 경로로 자동 커밋됩니다.
   - 수정 시 새 이미지를 선택하지 않으면 기존 이미지가 유지됩니다.

---

## 🛠️ 기술 스택

| 구분 | 사용 기술 |
|---|---|
| 마크업 | HTML5 |
| 스타일 | CSS3 (Custom Properties, Flexbox, Grid) |
| 스크립트 | Vanilla JavaScript (ES6+) |
| 에디터 | Quill.js (WYSIWYG) |
| 연동 | GitHub REST API v3 |
| 배포 | GitHub Pages |

---

## 📌 데이터 저장 방식

별도의 백엔드나 데이터베이스 없이, 각 HTML 파일 내 주석 블록에 JSON 형태로 데이터를 저장합니다.

```html
<!--__PROJECTS_DATA_START__
[{ "id": "...", "title": "...", ... }]
__PROJECTS_DATA_END__-->

<!--__ARTICLES_DATA_START__
[{ "id": "...", "title": "...", ... }]
__ARTICLES_DATA_END__-->

<!--__CERTS_DATA_START__
[{ "id": "...", "title": "...", "imgUrl": "...", ... }]
__CERTS_DATA_END__-->
```

항목을 등록·수정·삭제할 때마다 해당 JSON 블록이 갱신된 채로 GitHub에 커밋됩니다.  
수료증 이미지는 `assets/certificates/` 경로에 Base64로 디코딩되어 별도 파일로 저장됩니다.
