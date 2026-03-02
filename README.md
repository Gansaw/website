# HoJin Choi — Portfolio Website

비행 데이터 분석가이자 AI 엔지니어 최호진의 개인 포트폴리오 웹사이트입니다.  
항공우주 데이터 분석, 머신러닝 프로젝트, 인사이트 아티클을 담고 있습니다.

**🌐 Live Website**: [gansaw.github.io/website](https://gansaw.github.io/website)

---

## 📁 파일 구조

```
portfolio/
├── index.html       # 메인 페이지 (About / Skills / Education / Certificates / Contact)
├── project.html     # 프로젝트 목록 및 상세 뷰
├── article.html     # 아티클 목록 및 읽기 뷰
├── style.css        # 공통 스타일시트 (3개 페이지 공유)
└── README.md        # 프로젝트 문서
```

> `admin.html`은 이전 버전의 관리자 페이지로, 현재는 사용하지 않습니다.  
> 글쓰기 기능은 `project.html`, `article.html` 내부에 직접 내장되어 있습니다.

---

## ✨ 주요 기능

### 메인 페이지 (`index.html`)
- 히어로 섹션 (프로필 사진 포함)
- About Me (한/영 소개)
- Technical Skills (6개 카테고리)
- Education & Training 타임라인
- Certificates 그리드
- Contact 섹션 (이메일 / GitHub)

### 프로젝트 페이지 (`project.html`)
- 8개 기본 프로젝트 카드 (Aviation / AI·ML / Data Analysis)
- 카테고리 필터 버튼
- 카드 클릭 시 상세 모달 (Problem / Solution / Results / Technologies)
- **✍️ FAB 버튼** — 우측 하단 고정, 클릭하면 새 프로젝트 작성 모달 오픈
- 직접 작성한 프로젝트는 카드 하단에 🗑 삭제 버튼 표시

### 아티클 페이지 (`article.html`)
- 7개 기본 아티클 카드 (Insight / Paper Review)
- 카테고리 필터 버튼
- 카드 클릭 시 인페이지 상세 읽기 (HTML 본문 렌더링)
- **✍️ FAB 버튼** — 우측 하단 고정, 클릭하면 새 아티클 작성 모달 오픈
- 직접 작성한 아티클은 카드 하단에 🗑 삭제 버튼 표시

---

## ✍️ 글쓰기 기능 사용법

### 프로젝트 등록
1. `project.html` 접속
2. 우측 하단 **✍️** 버튼 클릭
3. 폼 작성:
   - 제목, 카테고리(Aviation / AI·ML / Data), 아이콘 이모지
   - 설명, Problem, Solution, Results
   - 기술 스택 (Enter 또는 `+ 추가` 버튼으로 태그 입력)
4. **🚀 프로젝트 등록** 클릭

### 아티클 등록
1. `article.html` 접속
2. 우측 하단 **✍️** 버튼 클릭
3. 폼 작성:
   - 제목, 카테고리(Insight / Paper Review), 예상 읽기 시간
   - 카드 미리보기용 요약 (2~3줄)
   - 본문 (HTML 태그 사용 가능)
4. **📤 아티클 등록** 클릭

### 지원 본문 HTML 태그
```html
<p>단락</p>
<h2>소제목</h2>
<ul><li>항목</li></ul>
<ol><li>번호 항목</li></ol>
<strong>굵게</strong>  <em>기울임</em>
<blockquote>인용문</blockquote>
<table><tr><th>헤더</th></tr><tr><td>셀</td></tr></table>
```

### 데이터 저장 방식
작성한 글은 **브라우저 localStorage**에 저장됩니다.
- 같은 컴퓨터·브라우저에서 새로고침·재방문 시에도 유지됩니다.
- 다른 기기나 브라우저에서는 공유되지 않습니다.
- 브라우저 데이터를 초기화하면 삭제됩니다.

---

## 🎨 커스터마이징

### 색상 변경 (`style.css`)
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

### 기본 프로젝트 수정 (`project.html`)
`<script>` 내부의 `PROJECTS` 배열을 직접 수정합니다:
```javascript
{ id: 9, title: '프로젝트 제목', desc: '설명', type: 'aviation',
  icon: '✈️', tech: ['Python', 'TensorFlow'],
  problem: '문제', solution: '해결책', result: '결과' }
```
`type` 값: `'aviation'` / `'ai'` / `'data'`

### 기본 아티클 수정 (`article.html`)
`<script>` 내부의 `ARTICLES` 배열을 직접 수정합니다:
```javascript
{ id: 8, category: 'insight', date: '2025년 7월 1일', readTime: '3분',
  title: '아티클 제목', excerpt: '요약 (카드 표시용)',
  body: `<p>본문 HTML</p>` }
```
`category` 값: `'insight'` / `'review'`

### 개인 정보 수정 (`index.html`)
- **이름 / 직함**: 히어로 섹션 텍스트
- **프로필 사진**: `<img src="data:image/jpeg;base64,...">` base64 값 교체
- **About Me**: `#about` 섹션 내 `<p>` 태그
- **이메일 / GitHub**: `#contact` 섹션 내 `.contact-item`

---

## 🚀 로컬 실행

```bash
# 1. 저장소 클론
git clone https://github.com/Gansaw/website.git
cd website

# 2. 로컬 서버 실행 (localStorage 정상 작동을 위해 필요)
python -m http.server 8080

# 3. 브라우저에서 접속
# http://localhost:8080
```

> ⚠️ `file://` 프로토콜(더블클릭 실행)로는 localStorage가 제한될 수 있습니다.  
> 반드시 로컬 서버 또는 GitHub Pages를 통해 실행하세요.

---

## 🚀 GitHub Pages 배포

1. GitHub 저장소에 아래 파일들을 모두 업로드합니다:
   ```
   index.html
   project.html
   article.html
   style.css
   README.md
   ```

2. 저장소 **Settings → Pages** 이동

3. **Source** → `Deploy from a branch` 선택

4. **Branch** → `main` / `/ (root)` 선택 후 **Save**

5. 몇 분 후 `https://<username>.github.io/<repository>/` 에서 확인

---

## 🛠️ 기술 스택

| 구분 | 사용 기술 |
|---|---|
| 마크업 | HTML5 |
| 스타일 | CSS3 (Custom Properties, Flexbox, Grid) |
| 스크립트 | Vanilla JavaScript (ES6+) |
| 아이콘 | Font Awesome 6 |
| 폰트 | Google Fonts — Inter |
| 저장소 | Browser localStorage |
| 배포 | GitHub Pages |

---

## 📱 브라우저 지원

| 브라우저 | 지원 여부 |
|---|---|
| Chrome (최신) | ✅ |
| Firefox (최신) | ✅ |
| Safari (최신) | ✅ |
| Edge (최신) | ✅ |
| 모바일 브라우저 | ✅ |

---

## 📞 Contact

- **Email**: gansaw12@gmail.com  
- **GitHub**: [github.com/Gansaw](https://github.com/Gansaw)
