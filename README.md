# HoJin Choi — Portfolio Website

비행 데이터 분석가이자 AI 엔지니어 최호진의 개인 포트폴리오 웹사이트입니다.  
항공우주 데이터 분석, 머신러닝 프로젝트, 인사이트 아티클을 담고 있습니다.

**🌐 Live Website**: [gansaw.github.io/website](https://gansaw.github.io/website)

---

## 📁 파일 구조

```
portfolio/
├── index.html       # 메인 페이지 (About / Skills / Career / Certificates / Contact)
├── project.html     # 프로젝트 목록 및 상세 뷰 (WYSIWYG 에디터 내장)
├── article.html     # 아티클 목록 및 읽기 뷰 (WYSIWYG 에디터 내장)
├── style.css        # 통합 스타일시트 (모든 페이지 및 에디터 스타일 공유)
└── README.md        # 프로젝트 문서
```

---

## ✨ 주요 기능

### ✍️ WYSIWYG 에디터 도입
- **Quill.js**를 도입하여 HTML 태그를 직접 입력할 필요 없이 **글꼴, 크기, 굵게, 기울임, 목록, 인용구, 링크** 등을 시각적으로 편집할 수 있습니다.
- `project.html`과 `article.html`의 글쓰기 및 수정 모달에 적용되어 있습니다.

### 🚀 GitHub API 실시간 연동
- 작성하거나 수정한 내용을 GitHub API를 통해 직접 레포지토리에 커밋하여 실시간으로 반영합니다.
- **게재 시간 자동 기록**: 글을 작성하거나 수정할 때 현재 날짜와 시간이 자동으로 기록되어 카드 하단에 표시됩니다.

### 🎨 개선된 UI/UX
- **카드 버튼 복구**: 각 프로젝트와 아티클 카드 하단에 'View Details →', 'Edit', 'Delete' 버튼을 배치하여 직관적인 관리가 가능합니다.
- **불필요한 정보 제거**: 아티클의 '읽기 시간' 등 불필요한 메타데이터를 제거하여 깔끔한 디자인을 유지합니다.
- **통합 스타일 관리**: 모든 스타일은 `style.css`에서 중앙 집중식으로 관리되어 유지보수가 용이합니다.

---

## ✍️ 사용법

### 🔑 GitHub Token 설정
글을 발행하거나 수정하려면 GitHub 토큰이 필요합니다.
1. 우측 하단 **🔑** 버튼 클릭
2. [GitHub Token 발급 페이지](https://github.com/settings/tokens/new?scopes=repo&description=portfolio-write)에서 `repo` 권한을 체크하여 토큰 발급
3. 발급된 토큰을 입력창에 넣고 **💾 저장** 클릭

### 글 작성 및 수정
1. 각 페이지 우측 하단의 **✍️** 버튼을 클릭하여 새 글을 작성하거나, 카드 하단의 **Edit** 버튼을 클릭하여 기존 글을 수정합니다.
2. 에디터를 사용하여 내용을 편집한 후 **등록/저장** 버튼을 클릭하면 GitHub에 즉시 반영됩니다.

---

## 🛠️ 기술 스택

| 구분 | 사용 기술 |
|---|---|
| 마크업 | HTML5 |
| 스타일 | CSS3 (Custom Properties, Flexbox, Grid) |
| 스크립트 | Vanilla JavaScript (ES6+) |
| 에디터 | **Quill.js (WYSIWYG)** |
| 연동 | **GitHub REST API** |
| 배포 | GitHub Pages |
