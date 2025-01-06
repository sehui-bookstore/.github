  ## 온라인 도서 쇼핑몰 2조핑 📖
- 개발 기간 : 2024.10.14 ~ 2024.12.06 (약 8주)
- 배포 URL : ejoping.shop

<br>

## 프로젝트 소개

- 도서 쇼핑몰 프로젝트입니다.
- 도서 조회, 주문, 결제가 가능합니다.

<br>

## 팀원 구성👨‍👩‍👧‍👦
<div align="center">

| **이한빈** | **양준하** | **박채연** | **이유현** | **이승준** | **이초은** | **정세희** | **김연우** |
| :------: | :------: | :------: | :------: | :------: | :------: | :------: | :------: |
| [<img src="https://avatars.githubusercontent.com/u/99483558?s=96&v=4" height="80" width="80"> <br/> @LuKaBery](https://github.com/LuKaBery) | [<img src="https://avatars.githubusercontent.com/u/100835168?s=96&v=4" height="80" width="80"> <br/> @Ori-Gui](https://github.com/Ori-Gui) | [<img src="https://avatars.githubusercontent.com/u/111040042?s=96&v=4" height="80" width="80"> <br/> @yeonicy](https://github.com/yeonicy) | [<img src="https://avatars.githubusercontent.com/u/125079725?s=96&v=4" height="80" width="80"> <br/> @00yuhyun](https://github.com/00yuhyun) | [<img src="https://avatars.githubusercontent.com/u/54736876?s=96&v=4" height="80" width="80"> <br/> @Sauter001](https://github.com/Sauter001) | [<img src="https://avatars.githubusercontent.com/u/69998481?s=96&v=4" height="80" width="80"> <br/> @choeunlee](https://github.com/choeunlee) | [<img src="https://avatars.githubusercontent.com/u/116075689?s=96&v=4" height="80" width="80"> <br/> @jungsehui](https://github.com/jungsehui) | [<img src="https://avatars.githubusercontent.com/u/113099598?s=96&v=4" height="80" width="80"> <br/> @YeonWooKimm](https://github.com/YeonWooKimm) |

</div>




<br>

## 1. 개발 환경

### 개발 환경
- 개발도구: Intellij IDEA - Ultimate
- 언어: Java 21 LTS<br>
- 빌드도구: Maven
- 개발
  - Spring Framework: 5.3
  - Spring Boot: 3.3.18
  - Spring Cloud
    - Spring Cloud Gateway
    - Spring Cloud Netflex(Eureka)
    - Spring Cloud Config
  - Spring Data
    - Spring Data JPA
    - Spring Data Elasticsearch
    - Spring Data Redis
  - JPA
    - QueryDSL
- 테스트
  - Junit5
  - AssertJ
  - Mockito
  - SonarQube
- 데이터베이스
  - MySQL: 8.0.25
  - Redis
- 검색엔진
  - Elastic Search: 7.11.1
- ERD
  - ERDCloud
- UI
  - BOOTSTRAP5
  - TOAST UI
- NHN Cloud
  - Instance
  - Secure Key Manager
  - Image Manager
  - Load Balancer
- 버전 및 이슈관리 : Github, Github Issues, Github Project
- [코드 컨벤션](https://github.com/orgs/nhnacademy-be7-2joping/projects/3?pane=issue&itemId=84107378)
  
<br>

## 프로젝트 규칙

### 1. 브랜치 전략🌴

- Git-flow 전략을 기반으로 main, develop 브랜치와 feature 보조 브랜치를 운용했습니다.
- main, develop, Feat 브랜치로 나누어 개발을 하였습니다.
    - **main** 브랜치는 배포 단계에서만 사용하는 브랜치입니다.
    - **develop** 브랜치는 개발 단계에서 git-flow의 master 역할을 하는 브랜치입니다.
    - **Feat** 브랜치는 기능 단위로 독립적인 개발 환경을 위하여 사용하고 merge 후 각 브랜치를 삭제해주었습니다.
 
### 2. 매일 9시30분 Scrum 진행

- Scrum 사항 및 공유 자료는 Gitjub Project에서 공유하였습니다.
- [Scrum](https://github.com/orgs/nhnacademy-be7-2joping/projects/5)

<br>

## 3. 역할 분담
    
### 🥇이한빈
- 회원
  - 회원가입 수정 탈퇴 뷰페이지 및 api 설계
  - 마이페이지 회원 등급, 쿠폰함, 내 좋아요 뷰페이지 및 api 설계
  - 배송지 추가 CRUD 설계 및 뷰페이지 제작 
- 쿠폰
    - 생일쿠폰 배치 작업 수행 BATCH, SCHEDULE, 멀티쓰레드 기술 적용 
- 예외 처리
  - bookServer : 예외처리된 내용을 errorresponse로 front server로 반환
  - frontserver: back으로부터 받은 code, message, type, url, data를 기반으로 Redirect, forward, errorPage 처리 
- 레이아웃 설계
  - 메인 페이지, 마이페이지 로그인 페이지 타임리프 레이아웃 디자인 및 설계
  - 로그인 유무에 따른 UI 변경
  - 사이드바, 네비게이션 구현

- wbs 및 github 관리 
  - wbs 설계 및 업무분배
  - scrum 및 기타 Convention 작성




### 👨🏻‍💻이승준

- DBA
  -  전체 DDL 작성 및 ER diagram과 DDL 수정
  -  DDL 정보 문서 작성 및 업데이트 

- 인프라
  - NHN Cloud Key manager 기반으로 MySQL 데이터베이스 정보 암호화 처리

- 인증/인가
  - Spring security 기반의 로그인
  - 로그아웃
  - 로그인 계정에 따른 관리자, 사용자 구분 및 권한별 리소스 접근 제한
  - 프론트에서 만료된 access token 재발급 요청 처리
 
- 주문
  -  회원/비회원 주문
  -  주문서 작성
  -  배송지 지정
  -  배송 날짜 지정
  -  주문 정보 등록

- 결제
  - Toss payment 적용
  - 결제 위젯 기반으로 결제


  
### ☘️양준하
- 카테고리
  - 등록, 수정, 조회, 삭제(약삭제) api 기능 구현 및 관리자 view
  - 카테고리 계층구조 활용 자식 카테고리 조회 
  - 페이징 처리


- 검색
  - ElasticSearch 인덱스 생성, 매핑 
  - ngram, nori, jaso 플러그인 분석기 설정 
  - logstash 활용 데이터 생성 
  - 형태소 분석, 텍스트 기반 검색 
  - 카테고리 기반 검색, 초성 기반검색 
  - 인기도순(조회수, 좋아요수), 신상품순(출시일순), 가격순, 평점순, 리뷰순 정렬 
  - 메인페이지, 검색페이지 view 도서 목록 구성, 페이징처리

- 도서 기여자 및 역할(지은이, 엮은이)
  - 등록, 수정, 조회, 삭제(약삭제) api 기능 구현 및 관리자 view
  - 페이징처리

- 배송 정책 및 배송 업체
  - 등록, 수정, 조회, 삭제(약삭제) api 기능 구현 및 관리자 view


### 👩🏻‍🦲정세희

- 인프라 구축
  - SSH 및 서버 설정
  - GitHub Actions 기반 CI/CD 파이프라인 구축
  - NGINX 서버 설정 및 HTTPS 적용

- 포인트 정책 관리 기능 구현
  - 포인트 정책의 등록, 조회, 수정, 삭제(비활성화) 기능 구현

- 포인트 적립 및 사용 기능 구현
  - 사용자에게 포인트를 적립하고 사용할 수 있는 기능 구현

- 포인트 내역 조회 기능 구현 
  - 사용자가 자신의 포인트 적립 및 사용 내역을 조회할 수 있는 기능 구현

- 쿠폰 정책 관리 기능 구현
  - 쿠폰 정책 등록(금액, %), 수정, 조회 기능 구현

### 👸🏾김연우
- 인증/인가
  - JWT 토큰 발급 및 관리 redis-session 구현
  - JWT 토큰 인증/인가 구현
  - 비동기요청을 이용한 토큰 재발급 구현
  - 토큰 활용 사용자 정보 api 전달 구현

- 장바구니
  - 장바구니 조회, 등록, 삭제
  - redis를 이용한 장바구니 세션 중앙화 구현
  - 장바구니 view 구현

- gateway
  - gateway 구현
 
- 주문 정보
  - 주문 정보 조회, 수정 api 구현
  - Admin 주문 정보 조회 view 구현

### 🙋🏻이초은
- 인프라
  - SSH 및 서버 설정
  - GitHub Actions 기반 CI/CD 파이프라인 구축
  - NGINX 서버 설정 및 HTTPS 적용
  - 메모리 제한 및 스왑 메모리 설정 

- 도서
  - 도서 등록 (직접 등록) / 수정 / 삭제 
     - api 구현 및 관리자 view 구현 
  - 도서 등록 (알라딘 API 활용) 
      - api 기능 구현 

- 이미지
  - nhn cloud 활용 local image file 업로드 구현
  - 포장지 이미지 등록, 수정, 삭제
  - api 기능 및 관리자 view 구현


### 👶🏻이유현
- 출판사
  - 등록, 조회, 수정, 삭제 기능 구현, 관리자 뷰 페이지 구현

- 도서
  - 도서 목록 조회, 상세 조회 기능 구현
  - 페이징 처리 기능

- 리뷰
  - 회원의 주문 내역에 따른 리뷰 작성 및 수정 기능 구현
  - 이미지 업로드 및 별점 기능 추가
  - 마이 페이지에 리뷰 내역 조회 뷰페이지 추가

- 주문 상세
  - 회원의 주문 내역에 따른 주문 상세 조회 기능 구현
  - 마이페이지에 주문 상세 내역 뷰 페이지 구현




### ☃️박채연

- 관리자
  -  관리자 페이지 레이아웃, css 적용
  -  관리자 페이지 기능 연결
  -  포장 정책
    - 포장 정책 등록, 조회, 수정, 삭제 api 구현 및 view 페이지 구현
  - 태그
    - 관리자 태그 등록, 조회, 수정, 삭제 api 구현 및 view 페이지 구현
  - 포인트 정책
    - 포인트 정책 조회, 수정, 약삭제 api 구현 및 view 구현
  - 쿠폰 정책
     - 관리자 view 페이지 구현
