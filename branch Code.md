# Git branch

## 1. branch 관련 명령어

> Git 브랜치를 위해 **root-commit을 발생**시키고 진행하세요.

```bash
$ git init
$ touch README.md
$ git add .
$ git commit -m 'README!'
$ git log # 확인
```



1. 브랜치 생성

    ```bash
    (master) $ git branch {브랜치명}
    ```

2. 브랜치 이동

    ```bash
    (master) $ git checkout {브랜치명}
    ```

3. 브랜치 생성 및 이동

    ```bash
    (master) $ git checkout -b {브랜치명}
    ```

4. 브랜치 삭제

    ```bash
    (master) $ git branch -d {브랜치명}
    ```

5. 브랜치 목록

    ```bash
    (master) $ git branch
    ```

6. 브랜치 병합

    ```bash
    (master) $ git merge {브랜치명}
    ```

	* master 브랜치에서 {브랜치명}을 병합

## 2. branch 병합 시나리오

> branch 관련된 명령어는 간단하다.
>
> 다양한 시나리오 속에서 어떤 상황인지 파악하고 자유롭게 활용할 수 있어야 한다.
>
> 웹 개발을 한다고 생각하세요.

### 상황 1. fast-foward (프리라이딩)

> fast-foward는 feature 브랜치 생성된 이후 master 브랜치에 변경 사항이 없는 상황

**about.html 페이지를 만드는 작업을 합니다.**

1. feature/about branch 생성 및 이동

   ```bash
   (master) $ git checkout -b feature/about
   (feature/about)
   ```

2. 작업 완료(about.html 파일 생성) 후 commit

   ```bash
   $ touch about.html
   $ git status
   $ git add .
   $ git commit -m 'Complete About page'
   ```

3. log 결과 확인

   ```bash
   $ git log
   ```


3. master 이동

   ```bash
   (feature/about) $ git checkout master
   (master)
   ```


4. master에 병합 > fast-foward (단순히 HEAD를 이동)

  ```bash
  $ git merge feature/about
  ```

5. 결과 확인(log) 

   ```bash
   $ git log
   ```

6. branch 삭제

   > 병합이 완료된 브랜치는 삭제합니다.
   
   ```bash
   $ git branch
   $ git branch -d feature/about
   $ git branch
   ```

브랜치에서 커밋

master 에서 병합할때 어떠한 커밋도 없었음


---

### 상황 2. merge commit (보고서 발표자료 각각)

> 서로 다른 이력(commit)을 병합(merge)하는 과정에서 **다른 파일이 수정**되어 있는 상황
>
> git이 auto merging을 진행하고, **commit이 발생된다.**

**메인 페이지를 만드는 작업을 합니다**

1. feature/main branch 생성 및 이동

   ```bash
   
   ```

2. 작업 완료 후 commit

   ```bash
   touch main
   ```

3. log 확인

   ```bash
   
   
   ```

4. master 이동

   ```bash
   
   ```

5. *master에 추가 commit 이 발생시키기!!*

   * **다른 파일을 수정 혹은 생성하세요!**

   ```bash
   
   ```

6. master에 병합 -> 자동으로 *merge commit 발생*

   ```bash
   
   ```

7. 결과 (log 확인)

   * vim 편집기 혹은 vs code 화면이 나타납니다.
   * 창을 종료해주시고, 커밋을 확인해보세요.

   ```bash
   
   ```

8. 그래프 확인하기

   ```bash
   
   ```

9. branch 삭제

   ```bash
   
   ```

브랜치에서 커밋

master에서 병합할때 어떠한 커밋이 있음(다른 파일 수정된 상황)

merge 커밋이 되어있음


---

### 상황 3. merge commit 충돌 (같이 보고서)

> 서로 다른 이력(commit)을 병합(merge)하는 과정에서 **같은 파일의 동일한 부분이 수정**되어 있는 상황
>
> git이 auto merging을 하지 못하고, 충돌 메시지가 뜬다.
>
> 해당 파일의 위치에 표준형식에 따라 표시 해준다.
>
> 원하는 형태의 코드로 직접 수정을 하고 직접 commit을 발생 시켜야 한다.

1. feature/board branch 생성 및 이동

   ```bash
   ```

   

2. 작업 완료(board.html) 후 commit (log 확인)

   * **README.md 파일을 수정하고 같이 커밋하세요.**

   ```bash
   ```

   


3. master 이동

   ```bash
   ```
   
   


4. *master에 추가 commit 이 발생시키기!!*

   * **README.md 파일을 수정 하세요!**
   
   ```bash
   ```
   
   
   
5. master에 병합

   ```bash
   ```
   
   


6. 결과 -> *merge conflict발생*

   > git status 명령어로 충돌 파일을 확인할 수 있음.
   
   ```bash
   ```
   
   


7. 충돌 확인 및 해결

   ```bash
   ```
   
   


8. merge commit 진행

   ```bash
   $ git commit
   ```

   * vs code 창 닫아주세요!

9. 그래프 확인하기

    ```bash
    ```

   


10. branch 삭제

    ```bash
    ```
    
    

브랜치에서 커밋

master에서 병합할때 어떠한 커밋이 있는데 이게 같은 파일이 수정된것. (파일을 열어서 충돌난 부분을 확인하여 고치고(내맘대로)/ add)

직접 merge 커밋해야함