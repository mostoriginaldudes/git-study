# git-study

### 원격 브랜치 로컬로 가져오기

```sh
git checkout -t origin/<remote-branch>

# example) git checkout -t origin/develop
```

### 브랜치명 확인하기

```sh
# local
git branch

#r emote
git branch -r
# git branch --remote

# all = local + remote
git branch -a
# git branch --all
```

### 브랜치 정보(커밋 메세지, 커밋 해쉬) 확인하기

```sh
# local
git branch -v

# remote
git branch -rv

# all
git branch -av
```

### 브랜치의 최근 커밋으로 되돌리기

```sh
git checkout -- .

# 권장
git restore -- .
```

### 브랜치 생성 후, 해당 브랜치로 전환

```sh
git checkout -b <new-branch>

# 권장
git switch -c <new-branch>
```

### 변경 사항을 commit하지 않고 잠시 다른 곳에 저장해두는 경우

```sh
# stash list 조회
git stash list

# git stash list에 있는 내용 다날리기
git stash drop

# 최근에 stack에 담아놓은 작업 내역을 가져오고, 지우기
git stash pop

# stack에 담긴 작업 내역을 반영하기
git stash apply <stash{id}>
```

### commit log 확인하기 (git log)

[참고글](https://git-scm.com/book/ko/v2/Git%EC%9D%98-%EA%B8%B0%EC%B4%88-%EC%BB%A4%EB%B0%8B-%ED%9E%88%EC%8A%A4%ED%86%A0%EB%A6%AC-%EC%A1%B0%ED%9A%8C%ED%95%98%EA%B8%B0)

```sh
# git log 1줄로 보기
git log --oneline # (+ 단축 Commit Hash ID)
git log --pretty=oneline # (+ 전체 Commit Hash ID)

# 그래프 형태로 보여줌 (위 명령어의 옵션과도 함께 사용 가능)
git log --graph

# 3 Commit 이전 시점부터 지금(HEAD)까지의 로그 보기
git log -3
git log -n 3
git log -n3

# 특정 시점의 커밋 보기

# 1일 전(24시간 전)까지의 commit 내역 출력
git log --before=1.day
git log --before=yesterday

git log --until=1.day
git log --until=yesterday
git log --until="one week ago"

# 1일 전(24시간 전)까지의 commit 내역 출력
git log --after="2021.10.19"
git log --since="2021-10-19"


# 특정 조건으로 보기

# Commit한 사람의 이름으로 검색
git log --oneline --author="이름"

# 특정 단어가 포함된 Commit 검색
git log --oneline --grep="단어"

# 특정코드가 수정된 Commit 검색
git log --oneline -S "특정코드" --patch

# 특정 파일을 수정한 커밋을 검색한다.
git log --oneline "파일이름" --patch

# 터미널에서 파일이름을 명령어와 구분하지 못하겠다고 할 때
git log --oneline --patch -- 파일이름


# 여러 옵션을 사용하는 경우 모든 조건을 만족하는 Commit만을 출력 (all-match)
git log --before=yesterday -S "console.log" --all-match
```

### 되돌리기 (git reset)

특정 Commit으로 또는 브랜치의 HEAD로 현재 작업 내용을 되돌리거나 staging, commit을 되돌리는 경우에 사용.

1. 옵션 설명

```sh
# 모든 작업 내역을 설정한 기준으로 되돌림, 모든 변경/수정 사항 사라짐.
git reset --hard
# 이 명령어 그대로 쓰는 경우에는 현재 브랜치의 최근 커밋으로 되돌림.

# 되돌리지만, 변경 내역은 unstaging 상태로 둠. 변경/수정 사항 사라지지 않음)
git reset --mixed # Default

# --mixed와 비슷, 하지만 변경 내역을 staging 상태로 둔다는 것이 차이.
git reset --soft
```

2. 사용법

```sh
# staging 취소하기

# 현재 staging되는 모든 파일 unstaging으로 변경
git reset

# 특정 파일만
git reset <file_name>

# 실수로 Commit 한 경우(push 이전)에 Commit 취소하기
git reset HEAD^
git reset HEAD~1 # 같은 의미 = 현재 가리키고 있는 Commit의 1개 이전의 Commit을 가리킴
```
