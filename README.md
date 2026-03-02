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

### 메인 페이지 (`index.html`)
- 히어로 섹션 (프로필 사진 포함)
- About Me (한/영 소개)
- Technical Skills (6개 카테고리)
- Career 타임라인
- Certificates 그리드
- Contact 섹션 (이메일 / GitHub)

### 프로젝트 페이지 (`project.html`)
- 카테고리 필터 버튼 (Aviation / AI·ML / Data Analysis)
- 카드 클릭 시 상세 모달 (Problem / Solution / Results / Technologies)
- **✍️ WYSIWYG 에디터** — Quill.js를 도입하여 제목, 본문, 글꼴, 크기 등을 시각적으로 편집 가능
- **🚀 GitHub 연동** — 작성한 내용을 GitHub API를 통해 직접 레포지토리에 커밋 및 반영

### 아티클 페이지 (`article.html`)
- 카테고리 필터 버튼 (Insight / Paper Review)
- 카드 클릭 시 인페이지 상세 읽기 (HTML 본문 렌더링)
- **✍️ WYSIWYG 에디터** — Quill.js를 도입하여 복잡한 HTML 태그 입력 없이 편리하게 글 작성
- **📎 첨부파일 기능** — 파일 업로드 인터페이스 제공
- **📤 GitHub 연동** — GitHub Personal Access Token을 사용하여 실시간 글 발행

---

## ✍️ 글쓰기 및 수정 기능 사용법

### 🔑 GitHub Token 설정
글을 발행하거나 수정하려면 GitHub 토큰이 필요합니다.
1. 우측 하단 **🔑** 버튼 클릭
2. [GitHub Token 발급 페이지](https://github.com/settings/tokens/new?scopes=repo&description=portfolio-write)에서 `repo` 권한을 체크하여 토큰 발급
3. 발급된 토큰을 입력창에 넣고 **💾 저장** 클릭 (브라우저에 안전하게 저장됩니다)

### 프로젝트/아티클 등록 및 수정
1. 각 페이지 우측 하단의 **✍️** 버튼 클릭
2. **WYSIWYG 에디터**를 사용하여 본문 작성:
   - 상단 툴바를 통해 **글꼴, 크기, 굵게, 기울임, 목록, 인용구, 링크** 등을 설정
   - HTML 코드를 직접 작성할 필요가 없습니다.
3. 내용 입력 후 **🚀 등록** 또는 **💾 저장** 버튼 클릭 시 GitHub 레포지토리에 즉시 반영됩니다.

---

## 🎨 커스터마이징

### 스타일 관리 (`style.css`)
모든 스타일은 `style.css`에서 중앙 집중식으로 관리됩니다.
```css
:root {
    --aviation-blue: #3b82f6;   /* 주요 강조색 */
    --accent-color:  #60a5fa;   /* 보조 강조색 */
    --bg-primary:    #0f172a;   /* 메인 배경 */
    --bg-secondary:  #1e293b;   /* 카드 배경 */
    --text-primary:  #f1f5f9;   /* 주 텍스트 */
    --text-secondary:#94a3b8;   /* 보조 텍스트 */
    --border-color:  #1e3a5f;   /* 테두리 */
}
```

---

## 🛠️ 기술 스택

| 구분 | 사용 기술 |
|---|---|
| 마크업 | HTML5 |
| 스타일 | CSS3 (Custom Properties, Flexbox, Grid) |
| 스크립트 | Vanilla JavaScript (ES6+) |
| 에디터 | **Quill.js (WYSIWYG)** |
| 아이콘 | Font Awesome 6 |
| 폰트 | Google Fonts — Inter |
| 연동 | **GitHub REST API** |
| 배포 | GitHub Pages |

---

## 📞 Contact

- **Email**: gansaw12@gmail.com  
- **GitHub**: [github.com/Gansaw](https://github.com/Gansaw)
