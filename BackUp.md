# 백업

> 언젠가는 데이터는 유실 될 수가 있기 때문에 언제나 데이터는 백업을 해놔야 한다.

## Git 백업

> 언제 어디서나 Git hub에 push한 데이터를 pull 할 수 있다. 

### 원격 저장소(Remote Repository)

> Github, Gitlab 등이 있으며 로컬에서 원격 저장소로 push 해놓아 저장 해놓을 수 있으며 언제 어디서나 push한 데이터를 가져올 수 있다.

* Github을 사용하면 버전관리가 된다.
* 종종 Github 보다는 가격적인 측면에서 GitLab을 사용하기도 한다. 
  * Github, Gitlab 둘다 오픈소스일 경우 무료로 사용 가능
  * 그러나 Gitlab이 무료로 이용할 수 있는 컨텐츠가 많다.

### 저장소 생성

#### Github 저장소 생성 과정

1. new repository 클릭

   ![first pic](C:\Users\LG\Documents\1.png)

   

2. repository 명 작성

   ![repository 명 생성](C:\Users\LG\Documents\2.png)

   * Description 부분에 설명 작성해 놓자!!

3. repository 생성 완료

   * Public은 모든 사람들에게 공유
   * Private는 내가 공유 하고 싶은 대상에게만 공유 But 비용이 발생

### 백업의 방법

1. HTTP 방식을 통하여 ___지역 저장소 -> 원격 저장소___
   * 배울것이 SSH비해 상대적으로 쉬움
2. SSH 방식을 통하여 ___지역 저장소 -> 원격 저장소___
   * 보안적으로 훨씬 강력함
   * 훨씬 편리함
   * But 배울것이 많아서 전문성 요구됨

### 원격저장소 연결

* Git 원격 저장소 연결

  ```shell
  git remote add [원격 저장소 별명] [원격 저장소 주소]
  ```

  * ex) git remote add test https://github.com/joon192/test.git

### Git Push[밀어 넣기]

* 어떤 저장소를 기본 저장소로 사용 할지 선택 하는 작업   

  ```shell
  git push --set-upstream [원격 저장소 별명] [브랜치 명]
  ```

  * ex) git push --set-upstream origin master

* 일반적으로 push 하는 작업

  ```
  git push [원격 저장소 별명] [브랜치 명]
  ```

  * ex) git push origin master

* Git push를 한다면 Git log들을 온라인으로도 확인 가능하다

### Git Clone[복제]

> 복제을 하게되면 여러대의 컴퓨터에 같은 파일의 상태를 유지 할수 있게 됨. push와 pull을 사용하여 공간의 제약 없이 작업이 가능하게 됨

* 이미 있는 것을 사용 하는것이기 때문에 clone을 사용

  ```shell
  git clone [깃헙 주소]/[내가 원하는 저장소]
  ```
  * 내가 원하는 저장소에 원격 저장소로부터 복제해서 지역 저장소로 복제가 됨

### Git pull[가져오기]

* 원격 저장소에 복제된 컨텐츠를 가져오기

  ```shell
  git pull [원격저장소 별명] [브랜치 명]
  ```

  * ex) git pull origin master 

* 일반적인 협업 과정은 Pull -> 작업 -> Commit -> Push 단계를 거친다.