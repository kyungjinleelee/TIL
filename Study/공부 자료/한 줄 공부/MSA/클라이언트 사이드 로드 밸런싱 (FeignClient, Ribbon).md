## 로드 밸런싱이란?

- 로드 밸런싱은 네트워크 트래픽을 여러 서버로 분산시켜 서버의 부하를 줄이고, 시스템의 성능과 가용성을 높이는 기술
- 서버 간 트래픽을 고르게 분배하여 특정 서버에 부하가 집중되는 것을 방지
- 종류: 클라이언트 사이드 로드 밸런싱, 서버 사이드 로드 밸런싱

## 클라이언트 사이드 로드 밸런싱이란?

- 클라이언트 사이드 로드 밸런싱은 클라이언트가 직접 서버를 선택하여 요청을 보내는 방식
- 클라이언트는 서버의 목록을 가지고 있으며, 이를 바탕으로 로드 밸런싱을 수행

<br>

## FeignClient란?

- FeignClient는 Spring Cloud에서 제공하는 HTTP 클라이언트로, 선언적으로 RESTful 웹 서비스를 호출할 수 있음
- Eureka와 같은 서비스 디스커버리와 연동하여 동적으로 서비스 인스턴스를 조회하고 로드 밸런싱을 수행

### FeignClient의 주요 특징

- **선언적 HTTP 클라이언트**: 인터페이스와 어노테이션을 사용하여 REST API를 호출할 수 있음
- **Eureka 연동**: Eureka와 통합하여 서비스 인스턴스 목록을 동적으로 조회하고 로드 밸런싱을 수행
- **자동 로드 밸런싱**: Ribbon이 통합되어 있어 자동으로 로드 밸런싱을 수행

<br>

## Ribbon이란?

- 넷플릭스가 개발한 클라이언트 사이드 로드 밸런서로, 마이크로서비스 아키텍처에서 서비스 인스턴스 간의 부하를 분산
- 다양한 로드 밸런싱 알고리즘을 지원하며, Eureka와 같은 서비스 디스커버리와 연동하여 사용

### Ribbon의 주요 특징

- **서버 리스트 제공자**: Eureka 등으로부터 서비스 인스턴스 리스트를 제공받아 로드 밸런싱에 사용
- **로드 밸런싱 알고리즘**: 라운드 로빈, 가중치 기반 등 다양한 로드 밸런싱 알고리즘 지원
- **Failover**: 요청 실패 시 다른 인스턴스로 자동 전환
