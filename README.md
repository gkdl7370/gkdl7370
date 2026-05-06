## 김지호 - 백엔드 개발자

Java와 Spring Boot를 중심으로 레거시 시스템 연동, 비동기 데이터 처리,
배치 기반 데이터 이관을 다뤄왔습니다.

요즘은 제가 진행했던 프로젝트들을 다시 정리하면서, 단순히 “이 기술을 써봤다”가
아니라 어떤 문제를 보고 어떤 방식으로 풀었는지 보여주는 방향으로 포트폴리오를
다듬고 있습니다.

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
**Data**: PostgreSQL, Oracle, Redis, SQLite  
**Infra**: Docker, Linux, GitHub Actions

---

### 프로젝트

| 저장소 | 정리한 내용 |
| --- | --- |
| [MassFlux-Gateway](https://github.com/gkdl7370/MassFlux-Gateway) | Netty 기반 TCP 패킷 처리, 게이트웨이 핸들러 테스트, 검증 노트 |
| [Data-Flux](https://github.com/gkdl7370/Data-Flux) | Spring Batch 데이터 분해 로직, JDBC Writer, processor 테스트, 벤치마크 정리 |
| [migration](https://github.com/gkdl7370/migration) | Oracle to PostgreSQL 이관 구조, 동적 SQL 생성 테스트, 이관 검증 노트 |
| [One-Core-Architecture](https://github.com/gkdl7370/One-Core-Architecture) | 레거시 payload 정규화, 경보 정책 분리, 설계 샘플 정리 |
| [kafka-practice](https://github.com/gkdl7370/kafka-practice) | Kafka producer/consumer 실습, DLQ 분기 테스트 |
| [SimpleIoT.Gateway](https://github.com/gkdl7370/SimpleIoT.Gateway) | .NET 게이트웨이 현대화 실험, 파서 테스트, 저장소 정리 계획 |

---

### 현재 정리 방향

포트폴리오를 다시 보면서, README의 설명과 실제 코드 사이의 간격을 줄이는 데
집중하고 있습니다.

- 핵심 로직은 테스트로 검증하기
- CI에서 테스트를 건너뛰지 않기
- 성능 수치는 측정 기준을 먼저 정리한 뒤 공개하기
- 학습 프로젝트와 실무형 프로젝트의 범위를 분명히 나누기
