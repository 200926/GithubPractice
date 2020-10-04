# 깃 & 깃허브       (패스트캠퍼스 HTML/CSS, JavaScript 올인원 패키지 Online 수업을 들으며 노트한 내용입니다.)

# CLI & GUI 
GUI : 버튼 클릭을 통해 Git 명령을 실행할 수 있는 도구, CLI 보다 하기 쉽다. ex. 소스트리
그러나, CLI를 꼭 사용해야할 때가 있다.

# 깃

1.      pwd                     지금 폴더가 어디 있는지 확인
2.      cd ㅁㅁ / cd ..         cd = change directory / 상위 폴더로 이동        
3.      ls / ls -al             현재 폴더에 어떤 파일과 폴더들이 있는지 확인 / 숨겨진 파일까지 확인
4.      git init                여기에서 Git을 쓸거다! 라고 명령
5.      git add / git add .     내가 변경한 파일 중 올리길 원하는 것만 선택 / 전체 파일 추가학 싶을 때
6.      git commit -m "내용"    선택한 파일들을 한 덩어리로 만들고 설명 적어주기  
                                (커밋Commit = 하나의 버전, '의미있는 변동사항'을 묶어서 만듬)
7.      git log                 생성한 커밋 보기

기타.   *** Please tell me who you are. 에러가 나올 경우
        $ git config --global user.name "user name"  과  $ git config --global user.email "user e-mail"  입력


# 깃허브 에 프로젝트 올리기

로컬저장소 -> 원격저장소
원격저장소 : 다른 사람들도 접근하게 하기 위해 클라우드(원격저장소)에 올림, 함께 버전 관리 가능
GitHub 외에도 GitLab, BitBucket 등이 있다.

8.      GitHub에 로그인해서 저장소 생성
9.      git remote add origin 깃허브주소        내 컴퓨터 폴더에 GitHub 저장소 주소 알려주기
10.     git push origin master                  만든 커밋 푸시하기
11.     GitHub 사이트에 올라간 커밋 확인


# 깃허브 프로젝트 내 컴퓨터로 받기

12.     git clone 깃허브주소 .          .을 꼭 같이 적어줘야 따로 폴더 생성 없이 파일이 생긴다.
13.     rm -rf 폴더명                   폴더 삭제


# 깃허브 상대방의 변동사항 pull 하기
14.     git pull origin master



200926ne@DESKTOP-BGG9A9O MINGW64 ~                                                  
$ pwd                                                                                         1                         
/c/Users/200926ne                                                           
                                                                    
200926ne@DESKTOP-BGG9A9O MINGW64 ~  
$ cd ..                                                                                       2                

200926ne@DESKTOP-BGG9A9O MINGW64 /c/Users
$ cd ..

200926ne@DESKTOP-BGG9A9O MINGW64 /c
$ ls                                                                                          3
'$Recycle.Bin'/             pleiades-2019-12-java-win-64bit-jre_2020
'$SysReset'/               'Program Files'/
'$WinREAgent'/             'Program Files (x86)'/
 Config.Msi/                ProgramData/
'Documents and Settings'@   Projects_Spring/
 DumpStack.log.tmp          recovery/
 hiberfil.sys               Samsung/
 Intel/                     swapfile.sys
 OneDriveTemp/             'System Volume Information'/
 pagefile.sys               Users/
 PerfLogs/                  Windows/
 pleiades/                  workspace/
 
200926ne@DESKTOP-BGG9A9O MINGW64 /c 
$ cd workspace                                                                               2

200926ne@DESKTOP-BGG9A9O MINGW64 /c/workspace
$ ls
github/

200926ne@DESKTOP-BGG9A9O MINGW64 /c/workspace
$ cd github

200926ne@DESKTOP-BGG9A9O MINGW64 /c/workspace/github
$ ls
workspace_github_user1/  workspace_github_user2/

200926ne@DESKTOP-BGG9A9O MINGW64 /c/workspace/github
$ cd workspace_github_user1

200926ne@DESKTOP-BGG9A9O MINGW64 /c/workspace/github/workspace_github_u
$ git init                                                                                  4
Initialized empty Git repository in C:/workspace/github/workspace_gihub_user1/.git/

200926ne@DESKTOP-BGG9A9O MINGW64 /c/workspace/github/workspace_github_uer1 (master)
$ ls -al                                                                                    3
total 4
drwxr-xr-x 1 200926ne 197610 0 10월  4 20:52 ./
drwxr-xr-x 1 200926ne 197610 0 10월  4 20:12 ../
drwxr-xr-x 1 200926ne 197610 0 10월  4 20:52 .git/

200926ne@DESKTOP-BGG9A9O MINGW64 /c/workspace/github/workspace_github_uer1 (master)
$ git add README.md                                                                         5

200926ne@DESKTOP-BGG9A9O MINGW64 /c/workspace/github/workspace_github_user1 (master)
$ git commit -m "README.md 추가"                                                            6

*** Please tell me who you are.                                                             기타

Run

  git config --global user.email "you@example.com"                                          
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got '200926ne@DESKTOP-BGG9A9O.(none)')

200926ne@DESKTOP-BGG9A9O MINGW64 /c/workspace/github/workspace_github_user1 (master)
$ git config --global user.name "user name"

200926ne@DESKTOP-BGG9A9O MINGW64 /c/workspace/github/workspace_github_user1 (master)
$ git config --global user.email "user e-mail"

200926ne@DESKTOP-BGG9A9O MINGW64 /c/workspace/github/workspace_github_user1 (master)        6
$ git commit -m "READ.md 추가"
[master (root-commit) ec34f1c] READ.md 異붽?
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

200926ne@DESKTOP-BGG9A9O MINGW64 /c/workspace/github/workspace_github_user1 (master)        7
$ git log
commit ec34f1c56f7dfb97eb6964e980d8a5715dbc5bdc (HEAD -> master)
Author: user name <user e-mail>
Date:   Sun Oct 4 21:07:42 2020 +0900

    READ.md 추가

200926ne@DESKTOP-BGG9A9O MINGW64 /c/workspace/github/workspace_github_user1 (master)        5
$ git add .

200926ne@DESKTOP-BGG9A9O MINGW64 /c/workspace/github/workspace_github_user1 (master)        
$ git commit -m "메인 페이지 생성"
[master 1d9a7e8] 硫붿씤 ?섏씠吏 ?앹꽦
 2 files changed, 11 insertions(+)
 create mode 100644 app.js
 create mode 100644 index.html

200926ne@DESKTOP-BGG9A9O MINGW64 /c/workspace/github/workspace_github_user1 (master)
$ git config --global i18n.commitEncoding utf-8

200926ne@DESKTOP-BGG9A9O MINGW64 /c/workspace/github/workspace_github_user1 (master)
$ git config --global i18n.logOutputEncoding utf-8

200926ne@DESKTOP-BGG9A9O MINGW64 /c/workspace/github/workspace_github_user1 (master)
$ git log                                                                                   7
commit 1d9a7e8f03ba3a7ecd2939d48a5470c20bd29dbc (HEAD -> master)
Author: user name <user e-mail>
Date:   Sun Oct 4 21:08:53 2020 +0900

    메인 페이지 생성

commit ec34f1c56f7dfb97eb6964e980d8a5715dbc5bdc
Author: user name <user e-mail>
Date:   Sun Oct 4 21:07:42 2020 +0900

    READ.md 추가


 

200926ne@DESKTOP-BGG9A9O MINGW64 /c/workspace/github/workspace_github_user1 (master)       
$ git remote add origin https://github.com/200926/GithubPractice.git                       9

200926ne@DESKTOP-BGG9A9O MINGW64 /c/workspace/github/workspace_github_user1 (master)    
$ git push origin master                                                                   10
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (7/7), 707 bytes | 353.00 KiB/s, done.
Total 7 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/200926/GithubPractice.git
 * [new branch]      master -> master





200926ne@DESKTOP-BGG9A9O MINGW64 /c/workspace/github/workspace_github_user2                 12
$ git clone GithubPractice^C                                                                        

200926ne@DESKTOP-BGG9A9O MINGW64 /c/workspace/github/workspace_github_user2                 13
$ git clone https://github.com/200926/GithubPractice.git .
Cloning into '.'...
remote: Enumerating objects: 7, done.
remote: Counting objects: 100% (7/7), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 7 (delta 0), reused 7 (delta 0), pack-reused 0
Unpacking objects: 100% (7/7), 687 bytes | 62.00 KiB/s, done.