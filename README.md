## 김지호 - 백엔드 개발자

Java와 Spring Boot를 중심으로 레거시 시스템 연동, 비동기 데이터 처리,
배치 기반 데이터 이관을 다뤄왔습니다.

요즘은 예약·결제 흐름을 주제로 한 `SeatHub`를 만들면서, 기존에 다뤘던
도메인 분리, 배치 처리, 고처리량 요청 처리, 비동기 이벤트 처리, 운영 추적성을
하나의 백엔드 서비스 흐름 안에 다시 적용하고 있습니다.

**gkdl7370@naver.com**

---

### 관심 있게 보는 문제

**게이트웨이 / 시스템 연동**  
비표준 TCP 패킷, 장비 식별자 매핑, 외부 API 연동처럼 레거시 시스템과 신규
시스템 사이의 경계를 안정적으로 다루는 작업에 관심이 많습니다.

**배치 / 데이터 이관**  
Spring Batch, JDBC bulk insert, 동적 스키마 처리처럼 대량 데이터를 옮기고
검증하는 구조를 계속 공부하고 있습니다.

**도메인 중심 설계**  
외부 시스템의 규격이 자주 바뀌어도 코어 로직이 흔들리지 않도록, mapper,
policy, anti-corruption layer 같은 구조를 실험하고 있습니다.

---

### 기술 스택

**Backend**: Java 17, Spring Boot, Spring Batch, Netty, JPA, C#/.NET  
**Data**: MySQL, PostgreSQL, Oracle, Redis, SQLite  
**Infra**: Docker, Docker Compose, Linux, GitHub Actions

---

### 프로젝트

| 저장소 | 정리한 내용 |
| --- | --- |
| [SeatHub](https://github.com/gkdl7370/SeatHub) | 예약·결제 백엔드 시스템, 동시성 제어, 상태 전이, Docker 기반 로컬 실행 환경 |
| [MassFlux-Gateway](https://github.com/gkdl7370/MassFlux-Gateway) | Netty 기반 TCP 패킷 처리, 게이트웨이 핸들러 테스트, 검증 노트 |
| [Data-Flux](https://github.com/gkdl7370/Data-Flux) | Spring Batch 데이터 분해 로직, JDBC Writer, processor 테스트, 벤치마크 정리 |
| [migration](https://github.com/gkdl7370/migration) | Oracle to PostgreSQL 이관 구조, 동적 SQL 생성 테스트, 이관 검증 노트 |
| [One-Core-Architecture](https://github.com/gkdl7370/One-Core-Architecture) | 레거시 payload 정규화, 경보 정책 분리, 설계 샘플 정리 |
| [kafka-practice](https://github.com/gkdl7370/kafka-practice) | Kafka producer/consumer 실습, DLQ 분기 테스트 |
| [SimpleIoT.Gateway](https://github.com/gkdl7370/SimpleIoT.Gateway) | .NET 게이트웨이 현대화 실험, 파서 테스트, 저장소 정리 계획 |

---

### 현재 진행 방향

기존 프로젝트에서 따로 다뤘던 주제를 `SeatHub`에 다시 적용하면서, 설명과 코드,
테스트가 함께 남는 백엔드 프로젝트를 만드는 데 집중하고 있습니다.

- 예약·결제 상태 전이를 명확히 관리하기
- 같은 좌석에 대한 동시 예약을 테스트로 검증하기
- 관리자 검색 API에서 N+1과 인덱스 개선 과정을 남기기
- Docker Compose로 재현 가능한 로컬 실행 환경 유지하기
- 기존 프로젝트의 설계 경험을 하나의 서비스 흐름에 통합하기
