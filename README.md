# Spring Boot & JPA 기반의 간단한 쇼핑몰 프로젝트
## 03/02 
- 프로젝트 생성
- 소스트리앱을 이용한 프로젝트 형상관리 

### 깃 명령어 요약
- clone : 원격 저장소 복사
- add : 스테이지 영역에 작업 파일 추가
- commit : 세이브, 스테이지 영역의 파일들을 가지고 커밋 만들기
- push : 원격 저장소에 커밋하기

### 파일의 내용 되돌리기
- 특정 파일의 내용을 마지막 커밋으로 돌리고 싶다면 해당 파일 선택 후 `코드 뭉치 버리기` 선택

### 브랜치 변경하기
- branch: 기존 내용을 유지한 채 새로운 내용을 추가하고 싶을 때 사용
- checkout : 특정 브랜치(혹은 커밋)으로 돌아가고 싶을 때 사용
- 소스트리의 checkout : 브랜치 이름을 더블 클릭하는 것만으로 체크아웃 가능

## 병합하기 1
- 헤드 브랜치에 변경사항이 없고
- 병합 대상 브랜치가 헤드로부터 시작 경우
- 아주 쉽게 병합 가능 = Fast-foward

## 병합하기 2
- 헤드 브랜치에 추가적인 커밋이 생기는 경우
- 진짜 병합이 필요해 진다
- 충돌이 안나면 좋은데 충돌이 나도 겁내지 말자

## 충돌 해결하기
- 제일 중요한 점 : 겁내지 말아요!
- 같은 파일을 병합 대상 두 커밋에서 동시 수정했을 경우 충돌이 날 확률이 높다!
- 에디터 사용, 혹은 SourceTree를 사용해서 충돌 해결 가능하다.

## 커밋 되될리기

### reset 사용하기
- 장점 : 쉬워요
- 단점1 : 커밋이 날아간다
- 단점2 : 강제 푸시가 필요하다

### branch 만들어서 되돌리기
- reset 과는 달리 커밋이 사라지지않는다
- 장점: 쉽다
- 단점: 트리가 지저분해진다


### 현재 branch 내용 임시저장 후 체크아웃 테스트
- 테스트 커밋

1. 브랜치1에서 일단 (임시) 커밋을 한다
2. 브렌치2로 체크아웃해서 볼일을 본다
3. 다시 브랜치1로 돌아온다
4. 1의 작업을 이어서 마무리 짓는다
5. 커밋 덮어쓰기 (commit --amend) 를 한다
6. (옵션) 필요하다면 (push --force) 를 한다

- 의미 있는 커밋