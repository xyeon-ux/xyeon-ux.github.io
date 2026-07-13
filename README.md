# 정시연 포트폴리오

정적 HTML/CSS/JS로 구성된 포트폴리오 사이트입니다. 별도의 빌드 과정 없이 그대로 배포할 수 있습니다.

## 구성

```
index.html        메인 페이지 (Bento 그리드 + About)
JAJAK.html        JAJAK 케이스 스터디
MailringX.html    Mailring X 케이스 스터디
Moonshot.html     Moonshot 케이스 스터디
assets/           이미지 · 아이콘 · 로고
uploads/          목업 이미지
```

## GitHub Pages로 배포하기

1. 새 저장소를 만들고 이 폴더의 모든 파일을 루트에 올립니다.
   ```bash
   git init
   git add .
   git commit -m "Deploy portfolio"
   git branch -M main
   git remote add origin https://github.com/<사용자명>/<저장소명>.git
   git push -u origin main
   ```
2. GitHub 저장소 → **Settings → Pages** 로 이동합니다.
3. **Build and deployment → Source** 를 `Deploy from a branch` 로 설정합니다.
4. **Branch** 를 `main` / `/ (root)` 로 지정하고 **Save** 합니다.
5. 잠시 후 `https://<사용자명>.github.io/<저장소명>/` 에서 확인할 수 있습니다.

> 사용자 계정 사이트로 쓰려면 저장소 이름을 `<사용자명>.github.io` 로 만들면 `https://<사용자명>.github.io/` 로 접속됩니다.

## 로컬에서 미리보기

파일 경로가 모두 상대경로(`./assets/...`)이므로, 정적 서버로 열어야 이미지가 정상적으로 로드됩니다.

```bash
python3 -m http.server 8000
# http://localhost:8000 접속
```
