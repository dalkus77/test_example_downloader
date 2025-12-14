# Render 배포 가이드

Render에서 정적 사이트로 배포하는 방법입니다.

## 방법 1: render.yaml 사용 (권장)

### 1단계: GitHub 저장소 확인
- 저장소가 GitHub에 푸시되어 있어야 합니다
- 현재 저장소: https://github.com/dalkus77/test_example_downloader

### 2단계: Render에서 새 사이트 생성

1. **Render 대시보드 접속**
   - https://dashboard.render.com 접속
   - 로그인 (GitHub 계정으로 로그인 가능)

2. **새 Static Site 생성**
   - **New +** 버튼 클릭
   - **Static Site** 선택

3. **저장소 연결**
   - **Connect account** 또는 **Connect GitHub** 클릭
   - GitHub 저장소 권한 부여
   - 저장소 선택: `dalkus77/test_example_downloader`

4. **설정 입력**
   - **Name**: `test-example-downloader` (또는 원하는 이름)
   - **Branch**: `main`
   - **Root Directory**: (비워두기 - 루트 디렉토리 사용)
   - **Build Command**: (비워두기 - 빌드 불필요)
   - **Publish Directory**: `.` (현재 디렉토리)

5. **배포 시작**
   - **Create Static Site** 클릭
   - 배포가 자동으로 시작됩니다

### 3단계: 배포 완료 대기
- 배포가 완료되면 Render가 자동으로 URL을 생성합니다
- 예: `https://test-example-downloader.onrender.com`

## 방법 2: 수동 설정 (render.yaml 없이)

위의 방법 1과 동일하지만, render.yaml 파일이 있으면 Render가 자동으로 설정을 읽어옵니다.

## 배포 후 확인

배포가 완료되면:
1. Render 대시보드에서 사이트 상태 확인
2. 제공된 URL로 접속하여 테스트
3. "다운로드 시작" 버튼 클릭하여 기능 확인

## 자동 배포

- GitHub 저장소에 푸시할 때마다 자동으로 재배포됩니다
- Render 대시보드에서 배포 로그를 확인할 수 있습니다

## 주의사항

- Render의 무료 플랜은 일정 시간 비활성 시 슬리프 모드로 전환됩니다
- 첫 접속 시 약간의 지연이 있을 수 있습니다 (슬리프 모드에서 깨어나는 시간)
- 정적 사이트는 무료로 배포 가능합니다

## 문제 해결

### 배포 실패 시
1. Render 대시보드의 **Logs** 탭에서 오류 확인
2. **Settings** 탭에서 설정 확인
3. Root Directory와 Publish Directory가 올바른지 확인

### CORS 오류 발생 시
- GitHub에서 직접 파일을 다운로드하므로 CORS 정책에 따라 일부 브라우저에서 제한될 수 있습니다
- 이 경우 프록시 서버나 백엔드가 필요할 수 있습니다

