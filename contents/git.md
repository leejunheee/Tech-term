# Git

- [stash](#stash)
- fetch,full,clone 차이

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
