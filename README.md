# git-study

> 원격 브랜치 로컬로 가져오기

```sh
git checkout -t origin/<remote-branch>

# example) git checkout -t origin/develop
```

> 브랜치명 확인하기

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

> 브랜치 정보(커밋 메세지, 커밋 해쉬) 확인하기

```sh
# local
git branch -v

# remote
git branch -rv

# all
git branch -av
```

> 브랜치의 최근 커밋으로 되돌리기

```sh
git checkout -- .

# 권장
git restore -- .
```

> 브랜치 생성 후, 해당 브랜치로 전환

```sh
git checkout -b <new-branch>

# 권장
git switch -c <new-branch>
```
