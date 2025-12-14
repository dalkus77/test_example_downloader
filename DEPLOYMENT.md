# 배포 가이드

## GitHub Pages 배포 (권장)

GitHub Actions 워크플로우가 이미 설정되어 있습니다. 다음 단계를 따라 GitHub Pages를 활성화하세요:

### 1단계: GitHub Pages 활성화

1. GitHub 저장소로 이동: https://github.com/dalkus77/test_example_downloader
2. **Settings** 탭 클릭
3. 왼쪽 메뉴에서 **Pages** 클릭
4. **Source** 섹션에서:
   - **Deploy from a branch** 선택
   - **Branch**: `gh-pages` 또는 **GitHub Actions** 선택
5. **Save** 클릭

### 2단계: 자동 배포 확인

- `main` 브랜치에 푸시할 때마다 자동으로 배포됩니다
- Actions 탭에서 배포 상태를 확인할 수 있습니다
- 배포가 완료되면 `https://dalkus77.github.io/test_example_downloader`에서 접속 가능합니다

## 대안: Netlify 배포

### 방법 1: 드래그 앤 드롭 (가장 간단)

1. https://app.netlify.com/drop 접속
2. 프로젝트 폴더를 드래그 앤 드롭
3. 즉시 배포 완료!

### 방법 2: GitHub 연동

1. https://app.netlify.com 접속
2. **Add new site** > **Import an existing project**
3. GitHub 저장소 선택
4. 자동 배포 설정 완료

## 대안: Vercel 배포

1. https://vercel.com 접속
2. **Add New Project** 클릭
3. GitHub 저장소 선택
4. 자동 배포 설정 완료

## 배포 상태 확인

배포가 완료되면 다음 URL에서 접속할 수 있습니다:

- **GitHub Pages**: `https://dalkus77.github.io/test_example_downloader`
- **Netlify**: 배포 후 제공되는 URL
- **Vercel**: 배포 후 제공되는 URL

