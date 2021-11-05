1. Repository 저장할 **로컬 저장소 폴더** 생성

2. **GIT BASH 실행, **cd 폴더이름을 쳐서 경로 설정

3. **git clone 깃허브 원격저장소 주소 **(업데이트된 전체내용 다운로드 받기)

4. **git init** 로컬저장소 폴더에 Git 저장소를 생성 (.git) 폴더 생성

   * touch README.md 를 통해 파일 생성/ 업로드할 파일을 이동해서 붙여넣기
   * 파일이름은 다르게 저장하여 붙여넣을 것.

5. **git remote add origin 깃 원격저장소 주소** (code에서 주소 복사해서 붙여넣기)  

   * https://github.com/[유저네임]/[원격저장소 이름].git  을 통해 원격 저장소 정보를 추가

6. **git remote -v(조회)**

7. **git checkout -b 만들브랜치이름** (branch 만들기(master->브랜치로 변경됨))

8. **git add 파일명**을 통해 인덱스에 추가 (**add .** 전체파일 올리기)

   **git status**로 커밋될 준비가 된 파일 확인 가능

9. **git commit -m '메시지'**  을 통해 r파일 변경 추가 등 저장소에 기록

   * 커밋이란 파일이나 디렉토리 변경 내용을 저장소에 기록하는 작업

   **git status**로 커밋되었는지 확인한다. 

10. **git push origin master 또는 브랜치이름**  로컬 저장소 내용을 원격 저장소에 반영 

11.  **파일 수정 및 변경시** add다시하고 커밋하여 푸쉬하면 됨.
    5번부터 9번 다시 실행 (8번 빼고)

```
* 브랜치 삭제하기
git push origin --delete 브랜치 이름

* 브랜치 전환하기
git checkout 브랜치 이름

* 특정 브랜치 클론하기
git clone -b <branch명> <remote_repo 주소>
출처: https://info-lab.tistory.com/60 [:: IT School ::]

* 특정 브랜치 클론하기 
git clone -b master --single-branch https://github.com/zmfhd1/kulture2.git

```

> https://www.youtube.com/watch?v=tC8Xj_Bf8Fw github 기초 배우기 영상링크

