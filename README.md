## 📑 SSAFY 6기 공통 프로젝트 - Cotudy
#### Web RTC 기반 화상 스터디 플랫폼
![main-logo](https://user-images.githubusercontent.com/20656314/164156771-7333511a-a234-4bb5-8806-5c02117c1bc9.png)
<br>

### Cotudy 프로젝트팀을 소개합니다.
- [협업을 위해 노력하자.] 오윤기 😎
    - 팀장을 맡아 원팀이 되기위해 노력했습니다. 
- [6시가 지나도 끝나지 않는다.] 서형준 😤
	- 부족하면 더 열심히 하겠습니다.
- [발표는 나에게 맡겨라.] 최시열 🤠
	- 코터디 프로젝트의 발표는 걱정마세요. 
- [OpenVidu는 나에게!] 현종일 🧐
	- 코터디 WebRTC를 담당하겠습니다. 
- [UCC 영상제작은 껌] 전영서 🤓
	- 코터디 소개 UCC는 저에게 맡겨주세요.


### OverView
코로나시대에서 사람 만나기도 힘들고 공부는 해야하는데 하기 싫고 다른 사람들은 어떻게 공부하는지 궁금하시지 않나요?
학습열정이 식어가고 있는 사람들을 위해 저희 코터디가 왔습니다. 코터디에서 공부해서 학습열정을 다시 불태워보세요!

### Cotudy 교훈
당신의 경쟁자들은 지금도 공부하고 있습니다!!!

### 서비스개요
모두의 학습의지가 샘솟을 수 있는 스터디 플랫폼

## 코터디 서비스 화면

## 주요기능
### 1. WebRTC를 통한 실시간 화상 플랫폼
![main1](https://user-images.githubusercontent.com/20656314/164156776-4e0bc007-28d8-4d2f-8ab9-02c7efaf8eb5.png)
### 2. Teachable Machine pose을 통한 자세를 인식하여 학습기록
![주요기능2](/readme_assets/motion_detect.gif)
### 3. 공부시간을 활용하여 사용자들의 랭킹시스템
![주요기능3](/readme_assets/ranking_table.gif)

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
- Element Plus

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
![archi](https://user-images.githubusercontent.com/20656314/164156777-7d2e7dd4-965f-40db-805a-190da73f47b8.PNG)


### 기능 정의서
40db-805a-190da73f47b8.PNG)
![docs1](https://user-images.githubusercontent.com/20656314/164156782-2012e806-a45a-490c-ba72-4c2cb4e9bf74.PNG)
### 화면 설계서
![figma](https://user-images.githubusercontent.com/20656314/164156788-d0fd6574-e1ce-40c1-83f1-b86f0e98862b.PNG)

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
![erd](https://user-images.githubusercontent.com/20656314/164156800-b3da99b5-dfe9-44ad-885e-6506842b508c.PNG)


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


