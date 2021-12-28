# Git

- [stash](#stash)
- fetch,full,clone 차이
- reset, revert 차이 
- [브랜치](#브랜치)

---

- stash
  -  커밋하기는 충분치 않지만 저장은 해야하는 상황에 사용 -> git stash 
  -  임시 저장한 내용을 되돌릴때 -> git stash pop

- fetch,full,clone 차이 
  - fetch 
    - 단순히 원격 저장소의 내용을 확인하고 로컬 데이터와 병합은 하고싶지 않은 경우 
    - 원격 저장소의 최신 이력 확인 가능 
  
  - pull
    - fetch + clone 
    - 원격 저장소로부터 필요한 파일을 다운 + 병합 

  - clone 
    - pull + git remote add 

- reset , revert
  - reset 
    - 3가지 옵션 
      - soft : commit 된 파일들을 staging area로 돌려놓는다 -> commit 이전 상태 
      - mixed(default) : commit 된 파일들을 working directory로 돌려놓는다 -> add 이전 상태 
      - hard : commit된 파일 중 tracked 된 파일들을 working directory에서 삭제한다 -> 로컬 저장소에선 사라지지만 원격 저장소엔 남아있기때문에 충돌 발생 (팀 작업시엔 사용 금지)
  - revert
    - 이전 커밋 내역을 그대로 남겨둔 채 새로운 커밋 생성 
    - 다른 사람과 공유하는 브랜치에선 revert를 사용해야 히스토리가 바뀌지 않아 충돌이 발생하지 않는다.

- 브랜치 
  - 독립적으로 어떤 작업을 진행하기 위한 개념 
  - 필요에 의해 만들어지는 각각의 브랜치는 다른 브랜치의 영향을 받지 않기 때문에, 여러 작업을 동시에 진행할 수 있다. 
  - 다른 브랜치와 병합(Merge)함으로써, 작업한 내용을 다시 새로운 하나의 브랜치로 모을 수 있다.
