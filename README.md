
# ✅ Git_command_summary

---

## 📦 STAGE & SNAPSHOT  
작업 스냅샷과 Git 스테이징 영역

```bash
git status
# 변경된 파일 보기 (작업 디렉토리, 스테이징된 것 포함)

git add [file]
# 현재 상태의 파일을 다음 커밋에 추가 (스테이지)

git reset [file]
# 스테이징 취소, 작업 디렉토리의 변경 내용은 유지

git diff
# 변경되었지만 스테이지되지 않은 내용 확인

git diff --staged
# 스테이징된 내용과 커밋 예정 내용 비교

git commit -m "[descriptive message]"
# 스테이지된 내용을 커밋으로 저장
```

---

## ⚙️ SETUP  
모든 로컬 저장소에서 사용할 사용자 정보 설정

```bash
git config --global user.name "[firstname lastname]"
git config --global user.email "[valid-email]"
git config --global color.ui auto
```

---

## 📁 SETUP & INIT  
사용자 정보 설정, 저장소 초기화 및 클론

```bash
git init
# 기존 디렉토리를 Git 저장소로 초기화

git clone [url]
# URL을 통해 원격 저장소 복제
```

---

## 🌿 BRANCH & MERGE  
브랜치로 작업 격리, 컨텍스트 변경, 변경사항 통합

```bash
git branch
# 브랜치 목록 보기 (*는 현재 브랜치)

git branch [branch-name]
# 현재 커밋에서 새 브랜치 생성

git checkout [branch-name]
# 다른 브랜치로 전환

git merge [branch]
# 지정 브랜치의 변경사항 현재 브랜치에 병합

git log
# 현재 브랜치의 커밋 이력 보기
```

---

## 🌐 SHARE & UPDATE  
다른 저장소에서 업데이트 받아오기, 로컬 저장소 갱신

```bash
git remote add [alias] [url]
# 원격 저장소 별칭 추가

git fetch [alias]
# 원격 저장소의 모든 브랜치 가져오기

git merge [alias]/[branch]
# 원격 브랜치를 현재 브랜치에 병합

git push [alias] [branch]
# 로컬 브랜치 커밋을 원격 저장소에 전송

git pull
# 원격 브랜치의 변경사항 가져와 병합
```

---

## 🧭 TRACKING PATH CHANGES  
파일 제거 및 경로 변경의 버전 관리

```bash
git rm [file]
# 파일 삭제 및 커밋 준비

git mv [existing-path] [new-path]
# 파일 경로 변경 및 커밋 준비

git log --stat -M
# 이동된 경로 포함 커밋 로그 보기
```

---

## 🧰 TEMPORARY COMMITS  
임시로 변경사항 저장 후 브랜치 전환

```bash
git stash
# 변경된 내용 임시 저장

git stash list
# 스태시 목록 확인

git stash pop
# 스태시 최상단 내용 복원

git stash drop
# 스태시 최상단 내용 삭제
```

---

## ✏️ REWRITE HISTORY  
브랜치 리라이팅, 커밋 수정, 이력 삭제

```bash
git rebase [branch]
# 현재 브랜치의 커밋을 지정된 브랜치 뒤에 적용

git reset --hard [commit]
# 지정 커밋으로 작업 트리 및 스테이징 영역 재설정
```

---

## 🔍 INSPECT & COMPARE  
로그, 변경사항, 오브젝트 확인

```bash
git log
# 현재 브랜치 커밋 이력 보기

git log branchB..branchA
# branchA에는 있고 branchB에는 없는 커밋 보기

git log --follow [file]
# 파일의 변경 이력 (이름 변경 포함)

git diff branchB...branchA
# branchA와 branchB 간의 차이 보기

git show [SHA]
# SHA 오브젝트 보기
```

---

## 🚫 IGNORING PATTERNS  
불필요한 파일 스테이징/커밋 방지

```bash
git config --global core.excludesfile [file]
# 전역 무시 패턴 파일 설정
```

예시 `.gitignore` 내용:

```
logs/
*.notes
pattern*/
```

---

## 💡 참고 링크

- GitHub for Windows: [https://windows.github.com](https://windows.github.com)  
- GitHub for Mac: [https://mac.github.com](https://mac.github.com)  
- Git for All Platforms: [http://git-scm.com](http://git-scm.com)  
