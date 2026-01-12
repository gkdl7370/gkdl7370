# 🚀 Backend Engineer | Kim Ji-ho

안녕하세요 **데이터의 효율적인 흐름과 견고한 아키텍처**를 설계하는 데 가치를 두는 백엔드 개발자입니다.  
레거시 시스템의 현대화와 고성능 데이터 처리 엔진 구축을 통해 비즈니스 가치를 창출합니다. 

---

### 🛠 Tech Stack

- **Backend**: ![Java](https://img.shields.io/badge/Java-17-ED8B00?style=flat-square&logo=openjdk&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.3.x-6DB33F?style=flat-square&logo=spring-boot&logoColor=white) ![Netty](https://img.shields.io/badge/Network-Netty-007ACC?style=flat-square&logo=netty&logoColor=white) ![C#](https://img.shields.io/badge/C%23-239120?style=flat-square&logo=c-sharp&logoColor=white)
- **Infrastructure**: ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white)
- **Database**: ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

---

### 🌟 Project Highlights

#### 1. [MassFlux-Gateway](https://github.com/gkdl7370/MassFlux-Gateway) (C# to Java Migration)
**"레거시 수신 엔진을 현대화하여 동시 처리 성능 200% 혁신"** 
- **핵심 성과**: 
  - 초당 패킷 처리량 **200% 향상** (15K → 45K PPS) 및 지연 시간 **70% 감소** 
  - Netty 기반의 **Zero-copy 파싱** 구조 설계로 CPU 점유율 25% 최적화 
  - Docker Multi-stage 빌드를 통해 이미지 용량 **65% 경량화** (600MB → 210MB) 
- **Troubleshooting**: JDK 17 마이그레이션 시 `tools.jar` 부재 문제를 Maven Wrapper 도입으로 해결하여 빌드 환경 독립성 확보 

#### 2. [Excel-to-DB Loader](https://github.com/gkdl7370/SimpleIoT.Gateway) (ETL & Automation)
**"산업용 시계열 데이터의 자동 정규화 및 적재 도구 개발"** 
- **핵심 성과**: 
  - 24시간 가로 형태의 데이터를 개별 시간 레코드로 변환하는 **ETL 파이프라인** 구축 
  - 이기종 데이터(Excel to PostgreSQL) 매핑 자동화로 데이터 적재 시간 **90% 이상 단축** 
  - 관심사 분리(SoC)를 적용한 레이어드 아키텍처 설계로 유지보수성 향상

### 📈 Solving Challenges
- **Baekjoon Online Judge**: Silver 2 ~ Gold 3 수준의 알고리즘 문제 풀이를 통한 논리적 사고 훈련
- **Continuous Learning**: 산업용 시계열 데이터 자동 적재 및 성능 벤치마킹 연구 수행

---

### 📡 System Architecture (MassFlux-Gateway)

```mermaid
graph TD
    subgraph "Ingest & Process Layer"
        Sensor["📡 Industrial Sensors"]
        Netty["⚡ Netty Engine (TCP 8003)"]
        Decoder["⚙️ Decoder (Little Endian)"]
        Handler["🧠 Business Logic"]
    end

    subgraph "Forwarding Layer"
        Tomcat["🍃 Spring Boot (8080)"]
        API["👨‍💻 Monitoring / REST API"]
    end

    Sensor -->|Raw Binary| Netty
    Netty --> Decoder
    Decoder --> Handler
    Handler --> API
    Tomcat --> API

    style Netty fill:#e1f5fe,stroke:#0288d1,stroke-width:2px,color:#000
    style Tomcat fill:#e8f5e9,stroke:#388e3c,stroke-width:2px,color:#000
    style Handler fill:#fff9c4,stroke:#fbc02d,stroke-width:2px,color:#000
