# HoJin Choi — Portfolio Website

비행 데이터 분석가이자 AI 엔지니어 최호진의 개인 포트폴리오 웹사이트입니다.  
항공우주 데이터 분석, 머신러닝 프로젝트, 인사이트 아티클을 담고 있습니다.

**🌐 Live Website**: [gansaw.github.io/website](https://gansaw.github.io/website)

---

## 📁 파일 구조

```
website/
├── index.html       # 메인 페이지 (About / Skills / Career / Certificates / Contact)
├── project.html     # 프로젝트 목록 및 상세 모달 (WYSIWYG 에디터 내장)
├── article.html     # 아티클 목록 및 읽기 뷰 (WYSIWYG 에디터 내장)
├── style.css        # 통합 스타일시트
└── README.md        # 프로젝트 문서
```

---

## ✨ 주요 기능

### ✍️ WYSIWYG 에디터
- **Quill.js** 기반으로 HTML 태그 없이 글꼴·크기·굵기·목록·인용구·링크 등을 시각적으로 편집할 수 있습니다.
- `project.html`(상세 설명)과 `article.html`(본문) 모두에 적용되어 있습니다.

### 🚀 GitHub API 실시간 연동
- 작성·수정·삭제한 내용이 GitHub REST API를 통해 레포지토리에 직접 커밋되어 실시간으로 반영됩니다.
- 글 작성·수정 시 현재 날짜와 시간이 자동으로 기록됩니다.

### 🎨 UI/UX
- 각 카드 하단에 **View Details →** / **Edit** / **Delete** 버튼 배치로 직관적인 관리가 가능합니다.
- View Details 모달에서 긴 텍스트(Problem·Solution·Results 등)의 줄바꿈이 올바르게 표시됩니다.
- 모달 제목과 본문 사이 여백이 확보되어 가독성이 향상되었습니다.
- 전체 스타일은 `style.css`에서 중앙 집중식으로 관리됩니다.

---

## 🔁 GitHub 커밋 메시지 규칙

`project.html`과 `article.html` 모두 동일한 이모지 컨벤션을 사용합니다.

| 동작 | 커밋 메시지 |
|---|---|
| 새 항목 등록 | `✍️ Add project/article: <제목>` |
| 항목 수정 | `✏️ Edit project/article: <제목>` |
| 항목 삭제 | `🗑 Delete project/article: <제목>` |

---

## ✍️ 사용법

### 🔑 GitHub Token 설정
글을 발행하거나 수정하려면 GitHub Personal Access Token이 필요합니다.

1. 우측 하단 **🔑** 버튼 클릭
2. [GitHub Token 발급 페이지](https://github.com/settings/tokens/new?scopes=repo&description=portfolio-write)에서 `repo` 권한을 체크하여 토큰 발급
3. 발급된 토큰을 입력하고 **💾 저장** 클릭
   - 토큰은 브라우저 로컬 스토리지에만 저장되며 외부로 전송되지 않습니다.

### 📝 글 작성 / 수정 / 삭제

| 동작 | 방법 |
|---|---|
| 새 글 작성 | 우측 하단 **✍️** 버튼 클릭 |
| 글 수정 | 카드 하단 **Edit** 버튼 클릭 |
| 글 삭제 | 카드 하단 **Delete** 버튼 클릭 |

작성·수정 후 등록 버튼을 누르면 GitHub에 즉시 커밋되며, 약 3초 후 페이지가 자동으로 새로고침됩니다.

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
```

글을 등록·수정·삭제할 때마다 이 JSON 블록이 갱신된 채로 GitHub에 커밋됩니다.
