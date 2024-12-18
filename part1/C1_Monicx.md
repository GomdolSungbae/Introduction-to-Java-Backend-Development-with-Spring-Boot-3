# 1장. 스프링부트 시작하기

## 1.1 스프링 부트란

**스프링부트**는 자바 웹 프로그램을 더욱 쉽고 빠르게 만들기 위한 도구

- 자바 웹 프로그램을 만들기 위한 기능과 도구가 모여 있음
- [[스프링 프레임워크]]를 개선한 것
  - **개발 환경 간소화** :미리 설정된 스타터 프로젝트로 외부 라이브러리를 최적화해 제공하여 직접 외부 라이브러리를 연동하는 번거로움 감소
  - **웹 애플리케이션 서버 내장**: 내부에 [[웹 애플리케이션 서버(WAS)]]인 [[Tomcat]]을 가지고 있어 jar 파일로 간편하게 배포 가능

## 1.2 스프링 부트 프로젝트 생성

`Spring Initializr` 를 사용해 프로젝트 생성

1. https://start.spring.io 에 접속해서 프로젝트 생성
2. 프로젝트 세부 항목 설정
3. Dependecies에서 웹 도구 추가(Spring Web, H2 Database, Mustache, Spring Data JPA)
4. 프로젝트 다운로드 후 인텔리제이에서 빌드

## 1.3 웹 서비스 동작 원리 이해하기

### 클라이언트 - 서버 구조

- 클라이언트: 서비스를 사용하는 프로그램 또는 컴퓨터
- 서버: 서비스를 제공하는 프로그램 또는 컴퓨터
  웹 서비스는 클라이언트 요청에 따른 서버의 응답으로 동작. 웹 브라우저(클라이언트), 서버(스프링부트)

### localhost:8080

- localhost: 내 컴퓨터의 주소인 `127.0.0.1` 의 고유 지칭
- 8080: 스프링부트가 동작하는 기본 포트

---

# 추가

## 스프링 부트

> **스프링부트**는 엔터프라이즈급 애플리케이션을 빠르게 개발할 수 있도록 지원하는 스프링 프레임워크의 확장 도구

### 탄생 배경

- 기존 스프링 프레임워크는 설정이 복잡하고 시간이 많이 소요됨
- 개발자들의 생산성 향상을 위해 2014년 피보탈(pivotal)에서 출시
- 약속된 규칙을 통해 최소한의 설정으로 개발이 가능하게 설계됨

### 핵심 특징

1. **자동 구성(Auto Configuration)**

- 프로젝트에 추가된 라이브러리를 기반으로 자동으로 설정 구성
- `application.properties/yml` 파일에서 간단하게 설정 변경 가능

2. **내장 웹 서버(Embedded Web Server)**

- [[Tomcat]], [[Jetty]], [[Undertow]] 등 내장 웹 서버 지원
- 별도의 서버 설치 없이 독립적인 실행 가능
- Jar 파일로 배포 가능

3. **스타터 의존성(Starter Dependencies)**

- 일반적인 개발에 필요한 의존성을 모아둔 패키지를 제공
- spring-boot-starter-web, spring-boot-starter-data-jpa 등
- 라이브러리 버전 충돌 문제 해결

4. **스프링 액추에이터(Spring Actuator)**

- 애플리케이션의 상태, 퍼포먼스, 상태 등을 모니터링하고 관리하는 기능 제공
- 상태 확인, 메트릭 수집, 로그 레벨 조정 등
- 모니터링 정보를 통해 애플리케이션의 문제점 파악 및 성능 최적화 가능
