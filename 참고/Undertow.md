# Undertow

## 개요

Undertow는 Red Hat에서 개발한 Java 기반의 고성능 웹 서버. WildFly(이전의 JBoss) 애플리케이션 서버의 웹 서버로 사용되며, 비동기 논블로킹 아키텍처를 기반으로 설계.

## 주요 기능

1. HTTP 서버

   - HTTP/1.1 지원
   - HTTP/2 지원
   - WebSocket 지원
   - 서블릿 4.0 구현

2. 내장 기능

   - 리버스 프록시
   - 로드 밸런싱
   - 파일 서빙
   - WebSocket 컨테이너

3. 핸들러 체인
   - 유연한 요청 처리 파이프라인
   - 커스텀 핸들러 구현 가능
   - 필터 체인 구성

## 특징

- 비동기 논블로킹 아키텍처
- 높은 확장성과 성능
- 낮은 메모리 사용량
- 모듈식 설계
- 임베디드 사용 지원
- Spring Boot 지원

## 핵심 컴포넌트

1. Core

   - 기본 HTTP 처리
   - 비동기 IO 처리

2. Servlet

   - 서블릿 컨테이너 구현
   - JSP 지원

3. WebSocket
   - WebSocket 프로토콜 지원
   - 실시간 통신 기능

## 장점

- 뛰어난 성능
- 낮은 메모리 사용량
- 높은 확장성
- 유연한 설정
- 비동기 처리 최적화
- 마이크로서비스 친화적

## 단점

- 상대적으로 적은 문서화
- 학습 곡선이 높음
- 커뮤니티 규모가 작음
- 관리 도구 부족

## 사용 사례

1. 고성능 웹 서버

   - 대규모 트래픽 처리
   - 실시간 애플리케이션

2. 마이크로서비스

   - Spring Boot 애플리케이션
   - 클라우드 네이티브 서비스

3. 임베디드 서버
   - 애플리케이션 내장
   - IoT 플랫폼

## 다른 서버와의 비교

### Undertow의 강점

- 더 높은 성능
- 더 낮은 메모리 사용량
- 비동기 처리 최적화
- 모던한 아키텍처

### 설정 예시

```java
Undertow server = Undertow.builder()
.addHttpListener(8080, "localhost")
.setHandler(new HttpHandler() {
@Override
public void handleRequest(HttpServerExchange exchange) {
exchange.getResponseHeaders()
.put(Headers.CONTENT_TYPE, "text/plain");
exchange.getResponseSender()
.send("Hello World");
}
}).build();
server.start();
```

## 성능 최적화 팁

1. 버퍼 크기 조정
2. 워커 스레드 풀 설정
3. IO 스레드 수 최적화
4. 직접 버퍼 사용
5. 핸들러 체인 최적화

> 특히 고성능이 요구되는 환경이나 마이크로서비스 아키텍처에서 강점을 보이는 웹 서버. 비동기 논블로킹 아키텍처를 기반으로 하여 높은 성능과 낮은 리소스 사용량이 특징
