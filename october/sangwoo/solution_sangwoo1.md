## Week1

## #1
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
    * `git log -n 3`
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

## \#2

```

- 상황

오늘부터 스플린트를 시작했다. 너무 고된 하루였다.

오늘 작업을 마무리하고 commit 하였다.

...

push하려고 보니, 아뿔싸 commit message에 오타를 발견했다.

commit message를 수정해야겠다.

이때 필요한 명령어가 무엇인지 작성해보자.

(답안 작성 후, 일부러 commit message에 오타를 내고 해당 명령어를 이용하여 수정해보자)

````

<img width="506" alt="스크린샷 2021-10-17 오후 5 56 13" src="https://user-images.githubusercontent.com/46016511/137619748-2f2aefdb-af76-4487-81d2-722d21649f45.png">

* `git commit --amend` 입력 후, text 수정

<img width="525" alt="스크린샷 2021-10-17 오후 5 59 20" src="https://user-images.githubusercontent.com/46016511/137619916-8eb4406a-d0f4-40e3-b95a-b3d6ec3a2abd.png">
