## 📑 SSAFY 6기 공통 프로젝트 - Cotudy
#### Web RTC 기반 화상 스터디 플랫폼
![main-logo](/uploads/6f0cb796dfad2dc36fdf1a4bed2b4ed4/main-logo.png)
<br>

### Cotudy 프로젝트팀을 소개합니다.
- [원팀이 될 수 있도록 노력하자.] 오윤기 😎
    - 팀장으로서 원팀으로 만들기위해 노력했습니다. 
- [6시가 지나도 끝나지 않는다.] 서형준 😤
	- 부족하면 더 열심히 하겠습니다.
- 최시열
- 현종일
- 전영서


### OverView
코로나시대에서 사람 만나기도 힘들고 공부는 해야하는데 하기 싫고 다른 사람들은 어떻게 공부하는지 궁금하시지 않나요?
학습열정이 식어가고 있는 사람들을 위해 저희 코터디가 왔습니다. 코터디에서 공부해서 학습열정을 다시 불태워보세요!

### Cotudy 교훈
당신의 경쟁자들은 지금도 공부하고 있습니다!!!

### 서비스개요
#### 모두가 학습의지가 샘솟을 수 있는 스터디 플랫폼

## 코터디 서비스 화면

## 주요기능
	### 1. WebRTC를 통한 실시간 화상 플랫폼
	![주요기능1](/uploads/1e25a0acd0ece020785235e07c7c5037/주요기능1.png)
	### 2. Teachable Machine pose을 통한 자세를 인식하여 학습기록
	![주요기능2](/uploads/74d9b7df5f33a9756902d8f58eb5107b/주요기능2.png)
	### 3. 공부시간을 활용하여 사용자들의 랭킹시스템
	![주요기능3](/uploads/fd43965daa2aaa52be9affee31c16d89/주요기능3.png)

<br>

## 개발 환경
#### 💻BackEnd
- Intellij
- Spring-Boot : 2.5.7
- Spring-Boot-BPA
- Spring Security
- Java 11
- mysql : 8.0.22
- Lombok

#### ✨Front-End
- Visual Studio Code
- Vue.js 3.0
- ~~~[적어주세요]~~~

#### 🖱Web RTC
- ovenvidu 2.19.0
#### 🖱Pose Detection
- Teachable Machine
#### Infra
- AWS EC2 - Deploy Server
- docker
- jenkins
- docker-compose
- nginx

### 👨‍👩‍👧협업 툴
- GitLab
- Jira
- Nortion
- Mattermost
- Webex
- Discord

## 서비스 아키텍쳐
![아키텍처](/uploads/ca178967e12255795a7f53e9838da17a/아키텍처.PNG)


### 기능 정의서
![기능_정의서](/uploads/05cc2639649be6385bb976a3f826e786/기능_정의서.PNG)

### 화면 설계서
![figma](/uploads/0bfc585f4f085161548ddde4db6dc674/figma.PNG)

### Git 컨벤션
```
feat : 새로운 기능 추가
fix : 버그 수정
docs : 문서 수정
chore : 그 외 자잘한 작업
test : 테스트 코드
build : 시스템 또는 외부 종속성에 영향을 미치는 변경사항 (npm, gulp, yarn 레벨)
ci : CI관련 설정
style : 코드 의미에 영향을 주지 않는 변경사항 (포맷, 세미콜론 누락, 공백 등)
refactor : 성능 개선
```

### Code 컨벤션
- 클래스 및 인터페이스 이름 : Pascal Case
- Method 및 변수 이름 camel Case
- 의존성 주입 : 생성자 주입
	- @RequiredArgsConstructor를 사용
- REST API
	- 응답 요청 모두 String(PK, StudyTime 제외)
	

### GitLab Flow 브랜치 전략

### E-R Diagram
![erd](/uploads/ff52bb195f5434e7c702f89ea7f49f83/erd.PNG)

### EC2 포트 정리

|**PORT**|**이름**|
|:---:|:---:|
|443|HTTPS|
|80|HTTP - HTTPS로 리다이렉트(프론트 페이지지로 리다이렉트)|
|6443|Openvidu|
|3306|MySQL|
|8081|Jenkins|
|8080|Spring boot Docker Container|
|3000|Vue.js, NginX Docker Container|

### Cotudy's Wiki 
~~추가 예정입니다~~


### 팀원 역활
- 오윤기
	- ERD 설계, Entity 구현, 랭킹순위리스트 API 구현, 페이지처리, 공부시간 확인 API 구현, DB관리, Swagger 작성
- 서형준
	- 방관리 API 구현, Openvidu 서버배포, 회원가입 로그인 기능 구현, 회원관리API 구현, CI/CD 구현, HTTPS 설정
- 최시열
	- Figma를 이용한 와이어프레임 구현, 메인페이지(로비/헤더/풋터) 구현, 로그인/회원가인 구연, 발표
- 전영서
	- Figma를 이용한 와이어프레임 구현, 랭킹페이지 구현, UCC 제작
- 현종일
	- Figma를 이용한 와이어프레임 구현, Openvidu 활용한 스터디방 구현, TeachableMachine 활용한 동작감지 기능 구현, 마이페이지/랭킹 차트 구현


