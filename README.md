## **Overview**

### 💫 **프로젝트 기간** : 2023. 05. 29 ~ 2023. 07. 06

## 👊🏻 **Introduce**

### Save Game은

소비 절약을 위한 챌린지를 만들어 서로의 지출을 공유하며 절약에 대한 동기부여를 제공하는 서비스입니다

💰 카테고리 별로 지출을 기록하여 나만의 지출 가계부를 만들어보세요!

📢 목표 지출 금액 혹은 도전하고픈 카테고리 별 챌린지에 참여해보세요! 해당하는 챌린지가 존재하지 않는다면 직접 만들어서 참여자를 모집해보세요!

😀 오늘 사용한 지출 내역, 있었던 일을 다른 사람들과 나눠보세요! 함께 나누면 즐거움이 2배!

🥇절약왕은 누구? 누적 지출 금액에 따라 챌린지 내 순위가 매겨집니다. 절약왕이 될 수도, 낙오자가 될 수도 있어요. 당신의 운명은?

## 시연 영상

[녹화_2023_07_06_18_34_09_341.mp4](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/14a6d9b3-1773-4f40-91c8-5524cc7ee515/%EB%85%B9%ED%99%94_2023_07_06_18_34_09_341.mp4)

## Project

- 🌟 배포 링크 (https://save-game-jeongseonp.vercel.app/)

- ⚙ 프로젝트 아키텍쳐 ([https://miro.com/app/board/uXjVM_lbK](https://miro.com/app/board/uXjVM_lbKdw=/))

- 🐱 Github (https://github.com/save-game/frontend)
---
![Untitled](https://github.com/bidanee/frontend/assets/110444526/46a83f20-f70d-453d-83a1-93ee91e669d8)
---

## 🛠 기술 스택

### Frontend

- React
- Typescript
- Recoil
- React-Router-Dom
- React-Query
- browser-image-compression
- React-Datepicker
- React-Hook-Form
- yup
- React-Chartjs
- firebase

***Styles***

- Tailwind CSS
- Daisy UI
- Styled-Component
- React-icons

### Backend

- Language : Java 11
- Framework : Springboot
- Build Tool : Gradle
- DB : MySQL
- Test : Junit, Postman
- JPA
- Auth : Jwt, Spring Security
- Docker
- AWS(EC2, RDS)
- Kakao API
- Spring Scheduler
- QueryDSL

### CI / CD

- Deploy
    - Vercel
    - Docker
    - Cloud Service  : Google Cloud Platform
    - Jenkins
- Communication
    - Slack
    - Gather
    - Github
    

## 📋 ERD
![erd](https://github.com/bidanee/frontend/assets/110444526/959d7997-8d28-4abc-be59-f06af5ae670d)
## 🔗 담당 기능
- 회원가입 기능 : react-hook-form과 yup을 이용해 유효성 검사와 중복체크를 구현했습니다.
<p align="center"><img src="https://github.com/bidanee/frontend/assets/110444526/66632063-afd3-44bf-9905-6d42d73be149" width="300px" height="400px"></p>


- 챌린지
    - 필터 기능 :텍스트 입력, 카테고리 선택, 금액 설정 슬라이드, 날짜 선택 처럼 다양한 필터를 통해서 챌린지, 지출 내역을 찾을 수 있게 만들었습니다.
    - 등록 기능 : react-hook-form을 활용하여 새로운 챌린지 등록폼 작성했습니다.
    - 나가기 기능 
<p  align="center">
<img src="https://github.com/bidanee/frontend/assets/110444526/452dc73a-e03c-447e-90fc-730b425a6aa4" width="300px" height="400px">
<img src="https://github.com/bidanee/frontend/assets/110444526/59ee8724-741a-4cb2-961d-3340767eb197" width="300px" height="400px">
</p>
<p  align="center">
<img src="https://github.com/bidanee/frontend/assets/110444526/71c8740c-573a-4c26-9016-e1f7d0b209bb" width="300px" height="400px">
<img src="https://github.com/bidanee/frontend/assets/110444526/70af77a2-41aa-40f3-8052-e03e9a787ae4" width="300px" height="400px">
</p>


- 게시판 기능
    - 게시글 이미지 등록 : 사용자가 이미지를 선택하면 Input file에 onChange로 선택된 파일을 감지하여 URL.createObject메서드로 구한 로컬 url로 화면에 미리보기를 표시합니다. 이미지 용량을 줄이기 위해 Brower-image-compression으로 리사이징 후 firebase storage에 저장 및 firebase의 url을 구해 백엔드 서버에 저장했습니다.
    - 게시글 수정 / 삭제 : userQuery로 쿼리를 받아오고 useMutation을 사용하 Mutation onSuccess에 해당 쿼리 키를 invalidate하여 새로 데이터를 받아오도록해서 불필요한 데이터 요청을 방지했습니다.
<p align="center">
    <img src="https://github.com/bidanee/frontend/assets/110444526/1cf1c290-a52e-4a6f-bc29-77390dab37e7" width="300px" height="400px">
    <img src="https://github.com/bidanee/frontend/assets/110444526/4140ddcb-4d39-4701-b965-6d6686621651" width="300px" height="400px">
    <img src="https://github.com/bidanee/frontend/assets/110444526/76ed5aee-94e4-457c-98f9-994ac73dbe61" width="300px" height="400px">
</p>

- 가계부 기능
  - 필터 기능 : 월별, 기간별(최근 한달, 최근 3개월, 최근 6개월), 카테고리 별 필터를 구현하였습니다.
<p align="center">
    <img src="https://github.com/bidanee/frontend/assets/110444526/35b828e5-3b73-4511-ac23-f6c72a65b551" width="300px" height="400px">
    <img src="https://github.com/bidanee/frontend/assets/110444526/57351582-1f32-4c32-ac06-d21d8ab7cb9c" width="300px" height="400px">
    <img src="https://github.com/bidanee/frontend/assets/110444526/40f6dbf3-4507-425d-a354-730dae149007" width="300px" height="400px">
</p>

## **🌷 Bud 소개**

- 이단비 / FE
- 이상호 / FE
- 박정선 / FE
- 김성재 / BE
- 김창호 / BE
- 손진성 / BE

## 프로젝트를 마치며

프로젝트를 하면서 좀 더 공부해야 할 부분들도 보이고 팀원들과 소통하는 과정에서 많이 배웠습니다.
저의 목표는 맡은 바 최선을 다하자였는데 민폐를 안끼쳤으니 목표는 채운 듯 합니다.
이슈는 바로바로 기록해놔야 한다는 깨달음을 얻기도 했고 팀원들과 대화는 자주 할수록 좋다라는 것도 느꼈습니다.
이번 프로젝트로 많은 것을 얻어간 듯 합니다.
