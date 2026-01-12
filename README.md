# 👋 Hello, I'm Jiho Kim (Burin)

### 🚀 6th Year Backend Engineer | Platform Scalability & Data Integrity Specialist

안녕하세요 **플랫폼 확장성과 서비스 안정성**에 집중해 온 백엔드 엔지니어 김지호입니다.
파편화된 레거시 시스템을 현대화하고 정량적 지표를 바탕으로 데이터 조회 성능을 극대화하는 엔지니어링을 지향합니다.

---

### 🛠 Tech Stack

- **Backend**: ![Java](https://img.shields.io/badge/Java-17-ED8B00?style=flat-square&logo=openjdk&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.3.x-6DB33F?style=flat-square&logo=spring-boot&logoColor=white) ![JPA](https://img.shields.io/badge/JPA-Hibernate-59666C?style=flat-square&logo=hibernate&logoColor=white) ![Netty](https://img.shields.io/badge/Network-Netty-007ACC?style=flat-square&logo=netty&logoColor=white) ![C#](https://img.shields.io/badge/C%23-239120?style=flat-square&logo=c-sharp&logoColor=white)
- **Data**: ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white) ![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white) ![GA4](https://img.shields.io/badge/Google_Analytics_4-E37400?style=flat-square&logo=google-analytics&logoColor=white)
- **Infrastructure**: ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

---

### 🌟 Key Project Achievements

#### 1. One Core Platform (Data Integration & Optimization)
**"30여 종의 파편화된 데이터를 단일 도메인으로 통합하여 시스템 확장성 확보"**
- **DDD 기반 아키텍처**: 이기종 데이터를 Aggregate 중심의 단일 모델로 통합하여 플랫폼 기반 구축
- **성능 최적화**: PostgreSQL 실행 계획 분석 및 Redis 캐싱을 통해 **데이터 조회 성능 3배 향상** 및 DB 부하 30% 감소
- **데이터 기반 의사결정**: GA4 지표 분석을 통해 저활용 기능을 제거하고 운영 정책 우선순위 결정

#### 2. Event-Driven Messaging (Scalability & Async)
**"비동기 파이프라인 설계를 통한 장애 전파 차단 및 무중단 서비스 달성"**
- **성능 혁신**: Netty 기반 Java 마이그레이션으로 초당 패킷 처리량 **200% 향상** 및 지연 시간 70% 감소
- **연동 표준화**: 어댑터 패턴(Adapter Pattern)을 적용하여 신규 시스템 연동 기간을 **4주에서 1주로 단축(75% 개선)**
- **C# 미들웨어**: 고속 데이터 수집에 최적화된 C# 경량 미들웨어를 자체 개발하여 서버 자원 효율화

#### 3. Local-First Architecture (Data Integrity)
**"불안정한 네트워크 환경에서의 데이터 신뢰성 95% 이상 보장"**
- **양방향 동기화**: SQLite 기반 로컬 DB 선커밋 후 비동기 동기화 구조 설계로 데이터 유실 방지
- **무결성 확보**: 증분 동기화(Sync Delta) 및 타임스탬프 기반 충돌 해결 로직으로 **데이터 오류율 95% 감소**
- **효율 향상**: 데이터 검증 시각화 도구 도입으로 검증 리드타임 50% 단축

---

### 📈 External Activity & Problem Solving
- **External Advisor**: 서울연구원 DB 설계 및 데이터 분석 자문 지원 (연구 데이터 구조적 문제 해결)
- **Logic & Algorithm**: 백준(BOJ) Silver 2 ~ Gold 3 수준의 지속적 문제 풀이를 통한 논리 구조 강화
- **Engineering Philosophy**: AI 지원 개발(Gemini 등)을 통한 로직 검증 및 기술 문서화의 표준화 지향

---

### 📡 System Flow (Event-Driven Architecture)

```mermaid
graph LR
    subgraph "Ingest"
        Sensor["📡 Industrial Sensors"]
        Middleware["⚡ C# Middleware"]
    end

    subgraph "Core Service"
        Redis["📦 Redis Pub/Sub"]
        Netty["🚀 Java/Netty Server"]
        JPA["💾 JPA/PostgreSQL"]
    end

    Sensor -->|Binary Packet| Middleware
    Middleware -->|Async Publish| Redis
    Redis -->|Subscribe| Netty
    Netty -->|DDD Model| JPA

    style Middleware fill:#e1f5fe,stroke:#0288d1,stroke-width:2px
    style Redis fill:#ffebee,stroke:#c62828,stroke-width:2px
    style Netty fill:#e8f5e9,stroke:#388e3c,stroke-width:2px
