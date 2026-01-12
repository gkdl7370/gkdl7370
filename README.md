# 👋 Hello, I'm Jiho (Burin)

### 🚀 Backend Engineer | Efficiency & Stability Driven

안녕하세요, **데이터의 효율적인 흐름과 견고한 시스템 아키텍처**를 설계하는 데 가치를 두는 백엔드 개발자 김지호입니다.
현재 레거시 시스템의 현대화와 고성능 데이터 처리 엔진 구축에 집중하고 있습니다.

---

### 🛠 Tech Stack

- **Languages**: ![Java](https://img.shields.io/badge/Java-17-ED8B00?style=flat-square&logo=openjdk&logoColor=white) ![C#](https://img.shields.io/badge/C%23-239120?style=flat-square&logo=c-sharp&logoColor=white)
- **Frameworks**: ![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.3.x-6DB33F?style=flat-square&logo=spring-boot&logoColor=white) ![ASP.NET](https://img.shields.io/badge/.NET-512BD4?style=flat-square&logo=.net&logoColor=white)
- **Infrastructure**: ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

---

### 🌟 Featured Projects

#### [MassFlux-Gateway](https://github.com/gkdl7370/MassFlux-Gateway)
- [cite_start]**C# 레거시 엔진을 Java 17/Netty로 마이그레이션**하여 처리 성능 **200% 향상** [cite: 7]
- Zero-copy 파싱 및 Little Endian 호환성 확보를 통한 데이터 정밀도 최적화

#### [SimpleIoT.Gateway](https://github.com/gkdl7370/SimpleIoT.Gateway)
- 산업용 TCP 소켓 데이터를 수집하여 REST API로 중계하는 경량형 엔지니어링 툴
- Docker Multi-stage 빌드를 통해 이미지 용량 **60% 경량화**

---

### 📈 Solving Challenges
- [cite_start]**Baekjoon Online Judge**: Silver 2 ~ Gold 3 수준의 알고리즘 문제 풀이를 통한 논리적 사고 훈련 [cite: 8, 9]
- **Continuous Learning**: 산업용 시계열 데이터 자동 적재 및 성능 벤치마킹 연구 수행

---

### 📡 System Architecture (MassFlux-Gateway)

```mermaid
graph TD
    subgraph "External World"
        IoT["📡 IoT Devices"]
        Admin["👨‍💻 Admin / Monitoring"]
    end

    subgraph "MassFlux-Gateway Container (Java 17)"
        direction TB
        Netty["⚡ Netty Server<br>(TCP Port 8003)"]
        Tomcat["🍃 Spring Web MVC<br>(HTTP Port 8080)"]
        
        subgraph "Core Engine"
            Decoder["⚙️ Decoder (Little Endian)"]
            Handler["🧠 Business Handler"]
        end

        Netty --> Decoder
        Decoder --> Handler
        Tomcat --> Handler
    end

    IoT --> Netty
    Admin --> Tomcat
