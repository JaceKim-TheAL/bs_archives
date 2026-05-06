# Basement Stock Archives

- Desktop의 파일을 Github에 올리고, Laptop에서 관리
  - Desktop : File 형태의 자료
  - Labtop : Markdown 혹은 Html 형식의 자료


---
### INDEX
- [작업전 동기화](#작업전-동기화)
- [충돌이 발생시](#충돌이-발생시)
- [작업후 업로딩](#작업후-업로딩)

---
### 작업전 동기화 

**1. 현재 브랜치 확인**  
```cs
git branch
```  
→ 작업 중인 브랜치가 `main` 인지, `develop` 인지 확인  
  
**2. 원격 저정소 최신내용 가져오기**
```cs
git fetch origin
```
→ 원격 저장소의 최신 커밋들을 가져오지만, 아직 로컬 브랜치에는 반영되지 않습니다.  
  
**3. 로컬 브랜치에 병합**
```cs
git pull origin main
```
→ main 브랜치의 최신 내용을 가져와 현재 브랜치에 병합합니다.  
  (작업 브랜치가 `develop` 이라면  `git pull origin develop` )  
  
**4. 변경 사항 확인**
```cs
git status
```
→ 업데이트 된 파일, 충돌 여부 등을 확인합니다.

<br/>

[[TOP]](#index)

---
### 충돌이 발생시

- Git이 충돌 부분을 표시합니다 ( `<<<<<<< HEAD` 같은 표시).
- 수동으로 수정 후:
```cs
> git add .
> git commit 
```  
→ 충돌 해결 완료.

<br/>

- Origin이 존재하지 않는다는 에러 발생시
- 레포지토리 생성후 연결 과정에서 문제가 발생한 경우이며, 다시 연결시켜주면 해결이 가능
```cs
fatal: 'origin' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

> git remote add origin https://github.com/JaceKim-TheAL/bs_archives.git
```
- **git remote add origin [레포지토리 주소]**
  <br/> 를 입력하여 origin 저장소를 연결해주고 다시 git remote -v를 입력하여 확인해보면 origin 저장소가 잘 연결되어있다
- 그리고 다시 origin main 저장소로 push 하면 정상적으로 작동이 된다

<br/>

[[TOP]](#index)

---
### 작업후 업로딩

**1. git 에 파일 혹은 디렉토리 추가**
```cs
git add .  // 파일 or 디렉토리
```  

**2. 추가코드에 대한 메시지 기록**
```cs
git commit -m "업데이트 메시지"
```  

**3. 원격저장소에 최종 저장**
```cs
git push -u origin main
```  

<br/>

[[TOP]](#index)

---

