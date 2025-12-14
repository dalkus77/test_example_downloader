# 파일 다운로드 웹페이지

버튼 한 번 클릭으로 GitHub 파일을 다운로드하는 순수 프론트엔드 웹 애플리케이션입니다.

## 기능

- 버튼 클릭으로 GitHub 파일 자동 다운로드
- 깔끔한 UI 디자인
- 서버 없이 브라우저에서 직접 다운로드
- 정적 호스팅 지원 (GitHub Pages, Netlify, Vercel 등)

## 사용 방법

### 로컬 실행

`index.html` 파일을 브라우저에서 직접 열거나, 간단한 HTTP 서버로 실행할 수 있습니다:

```bash
# Python 3의 내장 서버 사용
python -m http.server 8000

# 또는 Node.js의 http-server 사용
npx http-server -p 8000
```

그 후 브라우저에서 `http://localhost:8000`으로 접속하세요.

### 정적 호스팅 배포

이 프로젝트는 순수 HTML/CSS/JavaScript로 구성되어 있어 어떤 정적 호스팅 서비스에도 배포할 수 있습니다:

- **GitHub Pages**: 저장소 설정에서 Pages 활성화
- **Netlify**: `index.html`을 드래그 앤 드롭
- **Vercel**: 프로젝트 폴더를 배포
- **Render**: Static Site로 배포

## 파일 구조

```
.
├── index.html            # 프론트엔드 페이지 (단일 파일)
└── README.md            # 이 파일
```

## 기술 스택

- **Frontend**: HTML, CSS, JavaScript (Vanilla JS)
- **배포**: 정적 호스팅 서비스

## 작동 원리

1. 사용자가 버튼을 클릭합니다.
2. JavaScript의 `fetch` API를 사용하여 GitHub에서 직접 파일을 다운로드합니다.
3. 다운로드된 파일을 Blob으로 변환합니다.
4. 브라우저의 다운로드 기능을 통해 파일을 저장합니다.

## 주의사항

- CORS 정책에 따라 일부 GitHub 파일은 직접 다운로드가 제한될 수 있습니다.
- 대용량 파일의 경우 다운로드 시간이 걸릴 수 있습니다.
