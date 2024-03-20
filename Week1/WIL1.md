Git은 버전 관리 및 협업을 위해 사용하는 오픈소스 소프트웨어라고 한다.

파일의 수정 로그를 추적하고 원하는 상태의 코드를 사용하기 위해 Git을 쓴다.

Untracked-Unmodified-Modified-Staged로 구성되는 파일의 생명주기

Git의 영역으로는
Working Directory, Staging Area, Repository가 있다.
또 Repository는 Local Repo-와 Remote Repo-로 나뉜다.

Git 저장소를 만드는 법
git init

Git으로 관리할 대상을 등록하는 법
git add

파일 수정 후 로컬 저장소로 옮기는 법
git commit

버전 관리 외, 협업을 위해 Github를 쓴다.
이슈 트래킹 / 코드 리뷰 / Github Actions로 CI/CD / Github Projects로 프로젝트 업무 관리

push = upload ?

터미널에서 powershell을 git bash로 바꾸는 것 잊지 말기

git 최초 설정으로 이름, 이메일 입력

파일 관리
1. 모든 파일 한 번에 등록 
   git add.
2. 하나씩 등록
   git add <파일명>
3. unstage로 되돌리기
   git rm --cached <file>
4. 파일 수정 후 로컬 저장소로 옮기기
   git commit

README.md 작성할 때는 실수했지만, commit message도 작성하는 법이 있음.
-type
새로운 기능을 추가한 경우 : feat
기존 코드를 개선한 경우 : refactor
버그를 수정한 경우 : fix
코드 외의 설정을 바꾼 경우 : chore
문서화 : docs
테스트 코드 : test

Git에 커밋하기
git commit -m "<commit message>"

이제 로컬에서만 말고 Github에 올리려면
Remote Repository를 만들어 Local과 연결 (이름 같게 설정 유의, Pusblic 설정)

git remote add origin <주소>
git branch -M main
git push -u origin main

git add <파일명>
git commit -m "commit message"
git push origin main

실습 Repository 링크 : 
<https://github.com/YujunOh/YujunOh>
