# Apache Tomcat

## 개요

Apache Tomcat은 Apache Software Foundation에서 개발한 오픈소스 [[웹 애플리케이션 서버(WAS)]]. Java Servlet, JavaServer Pages(JSP), WebSocket 등 Java EE 사양의 일부를 구현한 서블릿 컨테이너를 제공

## 주요 기능

1. 서블릿 컨테이너

   - Java Servlet API 구현
   - JSP 엔진 제공
   - WebSocket 지원

2. 웹 서버 기능

   - HTTP 서버 기능 내장
   - 정적 리소스 제공
   - 가상 호스트 지원

3. 관리 도구
   - 웹 기반 관리 콘솔
   - 서버 상태 모니터링
   - 애플리케이션 배포 관리

## 특징

- 경량화된 구조
- 독립 실행형 서버로 동작 가능
- 다양한 운영체제 지원
- 설정의 유연성
- 대규모 커뮤니티 지원
- 무료 오픈소스

## 주요 구성요소

1. Server

   - Tomcat의 전체 인스턴스를 나타냄

2. Service

   - 하나 이상의 Connector와 하나의 Engine으로 구성

3. Connector

   - HTTP/1.1
   - AJP
   - HTTP/2

4. Engine

   - 요청 처리를 위한 파이프라인 정의

5. Host

   - 가상 호스트 정의

6. Context
   - 웹 애플리케이션 설정

## 장점

- 가볍고 설치가 쉬움
- 무료로 사용 가능
- 풍부한 문서와 커뮤니티 지원
- 다양한 운영체제 지원
- 설정이 비교적 간단
- 개발 환경과의 높은 호환성

## 단점

- 전체 Java EE 스펙을 지원하지 않음
- 대규모 엔터프라이즈 환경에는 제한적
- 클러스터링 기능이 제한적
- 고급 관리 기능 부족
- 상용 WAS 대비 성능 제한

## 일반적인 사용 사례

- 개발 및 테스트 환경
- 중소규모 웹 애플리케이션
- Spring Boot 애플리케이션 실행
- 마이크로서비스 구축
