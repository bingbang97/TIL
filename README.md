# git

- 분산 버전 관리프로그램

- 리누스 베네딕트 토르발스가 개발(리눅스 개발자)
  
  

- 버전 : 컴퓨터 소프트웨어의 특정 상태

- 관리 : 어떤일의 사무 시설이나 물건의 유지 개량

- 프로그램 : 컴퓨터에서 실행될 떄 특정 작업을 수행하는 일련의 명령어들 모음

- 버전관리 : 컴퓨터 소프트웨어의 특정 상태들을 관리하는 것?



버전 관리프로그램의 역할

최종, 진짜 최종, 진짜진짜 최종, ''' => 날짜1 날짜2 날짜3 => 날짜1 변경사항1, 날짜2 변경사항2, 날짜3, 변경사항3 => 변경사항1, 변경사항2, 변경사항3, 날짜3

- 위에 과정을 실행하고 날짜3에서 날짜1을 보기위해 변경사항을 역으로 변경해주는 역할을 해줌



git의 최종 역할

- 코드의 히스토리를 관리하는 도구

- 개발되어온 과정 파악 가능

- ??



github 깃기반의 원격저장서비스 git이랑 같은 의미가 아님 



---



# CLI



CLI 

- Command Line Interface

- 명령어를 통해 상호작용

GUI

- Graphic User Interface

- 그래픽을 통해 상호작용



why CLI?

- gui가 cli보다 사용하기 쉽지만 단계가 많고 컴퓨터의 성능을 더 많이소모

- 수많은 서버/ 개발 시스템이 CLI를 통한 조작 환경을 제공



shell

- 운영자와 운영 체제의 내부(커널) 사이의 인터페이스를 감싸는 역할

- 즉 운영체제 상에서 다양한 운영 체제 기능과 서비스를 구현하는 인터페이스를 제공하는 프로그램



---



- cd	:	change directory

- touch	:	파일 생성

- mkdir	:	make directoty

- rm	:	remove

- rm -r	:	디렉토리까지 삭제

- start, open	:	파일 열기



---



절대 경로

- 루트 디렉토리부터 목적 지점까지 거치는모든 경로를 전부 작성한것

- 윈도우 바탕화면의 절대 경로 => C:/Users/ssafy/Desktop

상대 경로

- 현재 작업하고 있는 디렉토리를 기준으로 계산된 상대적 위치를 작성한것

- 현재 작업하고 있는 디렉토리가 C:/Users일 때 윈도우 바탕화면으로의 상대경로는 ssafy/Desktop

./ : 현재 작업하고 있는 폴더

../ : 현재작업하고 있는 폴더의 부모 폴더



---

### GIT 기본기

- README.md

  - 기본적으로 대문을 장식하는 역할
  - 보통 md 형식으로 작성함

- Repository

  - 특정 디렉토리를 버전 관리하ㅡㄴ 저장소

  - git init 명령어로 저장소 작성

    
특정 버전으로 남긴다 => **커밋**한다고 표현


- working directory
  - 내가 작업하고 있는 실제 디렉토리

- staging area
  - 커밋으로 남기고 싶은 특정버전으로 관리하고 싶은 파일이 있는 곳

- repository
  - 커밋이 저장되든곳


- git log
  - 깃의 로그 상태를 확인하는 기능
- git status
  - 깃 상태 확인가능

### github 이용 하는 방법

- add commit push 순서를 통해 서버에 저장을 한다
- git clone 링크 해서 자료 받기
- git push origin master (master 대신 main을 써야할 수 도 있음)
    깃헙 서버에 저장하는 방법

### git 기본 이용 방법

- git init
  - 비어있는 git을 생성한다.
- git add .
  - 변경사항을 전부 올린다.
- git remote add origin 깃헙링크
  -깃헙링크와 연동
- git add "file name"
  - file을 올린다.
- git commit -m "message"
  - message의 이름으로 커밋을한다.
- git push
  - 한번 업로드 후 메인이나 마스터 없이 가능

# Markdown

- 텍스트 기반의 가벼운 **마크업** 언어
- 문서의 구조와 내용을 같이 **쉽고 빠르게** 작성하고자 탄생



##  Basic Syntax

###  Heading

- 제목을 강조하기 위함
- `#` 을 앞에 붙여 사용함
- `#`의 개수에 따라 아래와 H1~H6

# H1

## H2

### H3

#### H4

##### H5

###### H6



### 텍스트 강조

`**굵게**`

**굵게**

`*기울이기*`

*기울이기*

`~~취소선~~`

~~취소선~~

`<u>밑줄</u>`

<u>밑줄</u>

`>주석`

>
>>

`--- 구분선`

---

표

'''
| 번호 |  이름  |   전화번호    |
| :--: | :----: | :-----------: |
|  1   | 홍길동 | 010-5555-9999 |
|  2   | 김길동 | 010-5646-8969 |
|  3   | 이길동 | 010-1544-7979 |
'''

| 번호 |  이름  |   전화번호    |
| :--: | :----: | :-----------: |
|  1   | 홍길동 | 010-5555-9999 |
|  2   | 김길동 | 010-5646-8969 |
|  3   | 이길동 | 010-1544-7979 |

#### 코드블럭(Code Block)

```python
import requests
url = 'https://www.dhlottery.co.kr/common.do?method=getLottoNumber&drwNo=1020'

response = requests.get(url).json()



for i in range(1, 7):

  key = f'drwtNo{i}'

  print(response.get(key))
```

- ` 백킥 세개 이용해서 열고 세개 이용해서 닫음

#### 링크

- 하이퍼링크 기능

- `[string](url)`으로 사용

- 그림의 경우 `![ string](이미지 url 입력)`

- 파일 경로를 넣어 다운로드 가능한 링크 제작도가능

- 사진 복사 붙여넣기도 가능 추가 어셋폴더가 생성되어 자동으로 저장이 됨

- [구글](https://www.google.com)

- [ssafy](https://edu.ssafy.com/edu/main/index.do)



  <img src="20220715.assets/tree-g0e64a3af4_1280.jpg" alt="이미지" style="zoom:33%;" />

  

<img src="20220715.assets/image-20220715120241102.png" alt="image-20220715120241102" style="zoom:80%;" />