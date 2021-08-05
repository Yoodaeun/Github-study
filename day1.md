# Github 특강

### [ DAY-1 ]

#### 1. 수업 개요
- 강사님: 해피해킹_김탁희 강사님
- Markdown 활용 및 문서작성
- Git을 활용한 버전관리
- 포트폴리오 관리
- 실습예제

***

#### 2. Markdown

- 2004년 존 그루버가 만든 텍스트 기반의 가벼운 마크업 언어.
- 최소한의 문법으로 구조화로 인해 읽기 쉽도록 디자인.
- 다양한 환경에서 변환되어 보여짐.
- 활용 예: Github, 기술블로그, 일반SW...

 #####      Markdown 문법
- Heading : 문서의 제목이나 소제목으로 사용 (# 1~6)
- List : 순서있는 리스트(ol)와 순서 없는 리스트(ul)로 구성
- Fenced Code block : 코드 블록에 특정 언어를 명시 (backtick 기호 3개 ```)
- Inline  Code block : 인라인에 활용하여 작성 (backtick 기호 양쪽에 1개씩 ``)
- Link : 링크를 작성 ('[문자열] (url)')
- Image : 사진을 첨부('! [문자열] (url)')
- Blockquotes : 인용문 작성 ('>')
- Table : 표 작성 
- text 강조: 굵게(bold), 기울임(ltalic)으로 특정 글자들을 강조 ('**, *')
- 수평선 : 작성 도중 수평선을 그어 구분가능 ('***, ---, ___') 

#####     다운로드 관련 자료
- [GitHub Flavored Markdown](https://github.github.com/gfm/)
- [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
- [Markdown Guide](https://www.markdownguide.org/)

***

#### 3. 버전관리
- 동일한 정보에 대한 여러 버전을 관리하는 것 (하나의 파일=> 버전기록/관리/릴리즈;업데이트)
- 분산 -> 자유/오픈 소스 -> Git(2005)
- Git 분산버전관리시스템(DVCS) 
![Git](C:\Users\USER\Desktop\git자료사진1.PNG)

#### 4. Git 기초 흐름
- Git 이란 
  - 분산버전관리시스템으로 코드의 버전을 관리하는 도구
  - 컴퓨터 파일의 변경(수정)사항을 추척하고 여러명의 사용자들 간에 해당 파일들의 작업을 조율
  
- 분산버전관리시스템(DVCS) 이란
  - 중앙집중식 버전관리시스템은 중앙에서 버전을 관리하고 파일을 받아서 사용
  - 원격저장소(remote repository)를 통해 협업하고, 모든 히스토리를 클라이언트들이 공유
  
- 흐름
  -  1)작업하고 2) add하여 Staging area에 모아 3) commit으로 버전 기록

  ![git자료사진2](C:\Users\USER\Desktop\git자료사진2.PNG)
-  파일관리
  - modified: 파일이 수정된 상태(add 명령을 통해 staging area로 이동)
  - staged: 수정한 파일을 곧 커밋할 것이라고 표시한 상태(commit 전 저장소)
  - committed: 커밋이 된 상태

- 기본 명령어
  1.  $ git  init  :저장소 만들기
  -  특정 폴더를 git 저장소(repository)를 만들어 git으로 관리
  -  .git 폴더생성
  -  git bash에서 (master)라는 표기 확인

  2. $ git  add < file name >  :작업 후 변경
  -  working directory 상의 변경 내용을 staging area에 추가하기 위해 사용
  -  untracked/modified 상태의 파일 staged로 변경

  3.  $ git  commit  –m <커밋메시지>  :변경 후 버전기록
  -  staged 상태의 파일들을 커밋을 통해 버전으로 기록
  -  특히 메시지는 변경(수정) 사항을 나타낼 수 있도록 '명확'하게 작성해야 함.
  
  4. $ git  status  :상태보기
  - Git 저장소에 있는 파일의 상태를 확인하기 위하여 활용
  - 파일의 상태를 알 수 있음
  • Untracked files
  • Changes not staged for commit • Changes to be committed
  • Noting to commit, working tree clean
  
  5. $ git  log  :상태보기
  - 현재 저장소에 기록된 커밋을 조회
  - 다양한 옵션을 통해 로그를 조회할 수 있음($ git log -1/ $ git log -oneline/ $ git log -2 --oneline)
  - 
  6. $ git  remote  add  origin  < url > 
  > 깃아, 원격저장소(remote)에 추가해줘(add). origin이라는 이름으로 url을.

  7. $ git push origin master < url >
  - github에 파일 릴리즈(업데이트)
  
  8. Github 활용
  - [Github Link: https://github.com](https://github.com/)
  - 

