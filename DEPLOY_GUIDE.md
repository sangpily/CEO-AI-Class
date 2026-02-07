# GitHub Pages 배포 가이드

## 📦 준비 완료!

강의 안내서를 GitHub Pages로 배포할 준비가 모두 완료되었습니다.
아래 단계를 따라 진행하시면 **5분 내에 온라인 사이트가 공개**됩니다.

---

## 🚀 배포 3단계

### 1단계: GitHub에서 새 Repository 만들기

1. **GitHub 로그인**: https://github.com 접속 후 로그인
2. **새 Repository 생성**:
   - 우측 상단 `+` 버튼 클릭 → `New repository` 선택
   - **Repository name**: `ceo-ai-class` (정확히 이대로 입력)
   - **Public** 선택 (Private으로 하면 무료 배포 안됨)
   - **Add a README file** 체크 해제 (이미 준비되어 있음)
   - `Create repository` 버튼 클릭

3. **Repository 주소 복사**:
   - 생성 후 나오는 페이지에서 HTTPS 주소 복사
   - 형식: `https://github.com/sangpily/ceo-ai-class.git`

---

### 2단계: 로컬 파일을 GitHub에 업로드

아래 명령어를 **순서대로** 터미널/명령 프롬프트에 입력하세요:

```bash
cd /home/claude/ceo-ai-class

git remote add origin https://github.com/sangpily/ceo-ai-class.git

git push -u origin main
```

**주의사항**:
- GitHub 인증을 요구하면 Username과 **Personal Access Token** 입력
- Password 대신 **Personal Access Token** 사용 필요 (GitHub 정책)

---

### 3단계: GitHub Pages 활성화

1. GitHub repository 페이지에서 **Settings** 탭 클릭
2. 좌측 메뉴에서 **Pages** 클릭
3. **Source** 섹션에서:
   - Branch: `main` 선택
   - Folder: `/ (root)` 선택
   - `Save` 버튼 클릭

4. **완료!** 1~2분 후 페이지 상단에 주소 표시:
   ```
   Your site is published at https://sangpily.github.io/ceo-ai-class/
   ```

---

## 🌐 최종 결과

**강의 안내서 URL**: https://sangpily.github.io/ceo-ai-class/

이 주소를:
- ✅ 이메일로 전송
- ✅ 카카오톡으로 공유
- ✅ SNS에 게시
- ✅ 명함에 QR코드로 인쇄

모두 가능합니다!

---

## 🔧 Personal Access Token 만들기 (필요시)

GitHub에서 password 대신 사용하는 인증 토큰입니다.

1. GitHub 로그인 → 우측 상단 프로필 사진 클릭
2. **Settings** 클릭
3. 좌측 메뉴 맨 아래 **Developer settings** 클릭
4. **Personal access tokens** → **Tokens (classic)** 클릭
5. **Generate new token** → **Generate new token (classic)** 선택
6. **Note**: "CEO AI Class Deploy" (메모용)
7. **Expiration**: 90 days (또는 원하는 기간)
8. **Select scopes**: `repo` 전체 체크
9. **Generate token** 버튼 클릭
10. **생성된 토큰 복사** (한 번만 보여지므로 안전한 곳에 저장!)

Push할 때 Password 입력란에 이 토큰을 붙여넣으세요.

---

## 📝 업데이트 방법 (향후)

강의 내용이 변경되어 HTML을 수정한 경우:

```bash
cd /home/claude/ceo-ai-class
# index.html 파일 수정 후
git add .
git commit -m "업데이트 내용 설명"
git push origin main
```

1~2분 후 자동으로 사이트에 반영됩니다!

---

## ❓ 문제 해결

### "Permission denied" 오류
→ Personal Access Token이 필요합니다 (위 가이드 참조)

### 사이트가 안 보여요
→ GitHub Pages 활성화 확인 (3단계)
→ 1~2분 대기 후 새로고침

### 404 Not Found
→ Repository 이름이 정확히 `ceo-ai-class`인지 확인
→ index.html 파일이 root에 있는지 확인

---

준비 완료! 이제 1단계부터 시작하세요! 🚀
