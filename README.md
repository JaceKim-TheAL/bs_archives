# Basement Stock Archives

- Desktop의 파일을 Github에 올리고, Laptop에서 관리
  - Desktop : File 형태의 자료
  - Labtop : Markdown 혹은 Html 형식의 자료


---
### 단계별 방법  

1. 현재 브랜치 확인  
```cs
> git branch
* main
```  
→ 작업 중인 브랜치가 `main` 인지, `develop` 인지 확인

2. 원격 저정소 최신내용 가져오기
```cs
> git fetch origin
```
→ 원격 저장소의 최신 커밋들을 가져오지만, 아직 로컬 브랜치에는 반영되지 않습니다.

3. 로컬 브랜치에 병합
```cs
> git pull origin main
```
→ main 브랜치의 최신 내용을 가져와 현재 브랜치에 병합합니다.  
(작업 브랜치가 `develop` 이라면  `git pull origin develop` )

4. 변경 사항 확인
```cs
> git status
```
→ 업데이트 된 파일, 충돌 여부 등을 확인합니다.

---

