## Week1

### #1
```

- 문제: 각 상황에 맞는 명령어 작성하기

1. 이 branch의 commit log를 보려고 한다. 어떤 명령어를 써야할까?

2. 이 branch의 최신부터 3개의 commit log만을 보려고 한다. 어떤 명령어를 써야할까? (2가지 답)

3. 이 branch의 어제 이전의 commit log를 보려고 한다. 어떤 명령어를 써야할까?

4. 이 branch의 특정일자 이전의 commit log를 보려고 한다. 어떤 명령어를 써야할까?

5. 이 branch의 특정일자 이후의 commit log를 보려고 한다. 어떤 명령어를 써야할까?

6. 이 branch의 특정일자 까지의 commit log를 보려고 한다. 어떤 명령어를 써야할까?

7. 이 branch의 특정일자 부터의 commit log를 보려고 한다. 어떤 명령어를 써야할까?

```

1. branch의 commit log
    * `git log`
2. 최신부터 3개의 commit log
    * `git log -3`
    * 
3. 어제 이전의 commit log
    * `git log --before=1.day`
4. 특정일자 이전의 commit log
    * `git log --before=2021.09.30`
5. 특정일자 이후의 commit log
    * `git log --after=2021.09.30`
6. 특정일자 까지의 commit log
    * `git log --until=2021.09.30` 
7. 특정일자 부터의 commit log
    * `git log --since=2021.09.30`


```text
cf) 참고로, until, before는 모두 특정일자를 포함하여 이전 커밋 로그를 보여준다.
반면, after, since는 모두 특정일자 다음날부터 이후를 보여준다.
```

