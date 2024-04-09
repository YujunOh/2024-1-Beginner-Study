- 지난 주 복습
  
  Issue, Branch, Pull Request, Merge
  
  Merge한 브랜치를 재활용하지 않기

  모든 브랜치 확인 git branch -a

  브랜치 생성 후 이동
  git checkout -b "<브랜치 이름>"

  Merge (Merge Commit, Squash and Merge, Rebase and Merge)

- git log
    - Commit Id
    - HEAD
- git status
- Commit 되돌리기
    - amend
    - reset
    - revert

#### git log
 commit 기록 최신 순 확인
<br> 옵션) --oneline : 각 커밋을 한줄에 요약

#### Commit Id
 여러 번 등장하는 내용
 <br>Commit 식별 코드
 <br>40자 길이의 16진수
 <br>SHA-1 해시 함수? 사용
 <br>(*Secure Hash Algorithm*)

 #### Head
 현재 작업 중인 위치
 작업 중인 브랜치의 최최근 commit
 다음 commit의 base가 되는 commit
 새로운 commit이 생기면 HEAD도 바뀐다.

 #### git status
 파일을 세 가지 상태로 분류
 * Changes to be committed
 * Changes not staged for commit
 * Untracked files

 #### Commit --amend
 마지막 commit 내용에 변경이 있을 때 사용함
 <br>완전 새로운 commit으로 대체되며, commit id도 바뀜
 <br>vim으로 진입하여 commit 메시지를 수정하게 됨
 <br>- **nano라는 에디터도 있는 듯**
 <br>- '-m' option으로 vim 진입하지 않고 commit 메시지 수정
 <br> git commit --amend -m “커밋 메시지”
 <br>- ‘--no-edit’ option으로 commit 메시지 수정 없이 commit 수정
 <br> git commit --amend --no-edit
 <br> **다른 사람이 작업 기반으로 삼고 있는 commit은 amend하면 안 된다.**

 #### Reset
 commit 제거 시 사용
 <br>3가지 옵션(soft, mixed(default), hard) 존재
 <br>git reset ‘--option’ “<commit id>”
 <br>--soft : 커밋만 취소, 변경 사항은 Staging Area로 돌아감
 <br>--mixed : Working Directory
 <br>--hard : 변경 사항을 모두 제거하고 이전 커밋으로 돌아감

 #### revert
 commit을 제거하지 않고 되돌린다
 <br>되돌리기 위한 새로운 commit이 만들어짐
 <br>--edit 옵션이 디폴트
 <br>--no-edit 편집기 진입 없이 바로 revert 가능

 #### reset vs revert
 reset은 commit을 삭제하므로 위험
 <br>commit을 공유하는 다른 브랜치에도 영향을 줄 수 있다
 commit을 삭제하기보다 생성하여 되돌리는 revert가 보다 안전하다.

