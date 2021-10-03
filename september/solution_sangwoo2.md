

### 상황

* week1-sep 브랜치를 과거에 pull을 받아온 상황.
* 그 상태에서 로컬에서 작업을 진행했는데(커밋), 다른 분이 week1-sep에 업데이트를 하여 원격 브랜치의 코드가 변한 상황
* 이 상황을 모르고, 최근에 다시 작업을 진행하기 위해 pull을 받았는데, 충돌이 났다.

![스크린샷 2021-09-21 오후 3 20 36](https://user-images.githubusercontent.com/46016511/134121371-76d18760-fa85-4b7f-8eec-8f49ff0a49d3.png)



### 해결

1. 원격 레포지토리와 로컬 레포지토리가 오랫동안 동기화가 안된 상태이므로, 먼저 싱크를 맞춰준다.

   ```
   git fetch --prune origin
   ```

   * ``` git fetch --all --prune``` 
   * ```git fetch --all -p```
   * --all 을 통해 origin 뿐 아닌, upstream 등의 레포지토리와도 싱크를 맞출 수 있다.

2. 동기화 된 remote tracking branch (origin/week1-sep) 과 로컬 브랜치를 일치시킨다.

   ```
   git reset --hard origin/week1-sep
   ```

   

