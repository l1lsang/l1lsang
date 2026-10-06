<div align="center">

<img src="https://github.com/l1lsang.png" width="96" style="border-radius:50%"/>

# Jang Gyeongmin

### Full-Stack Developer · Product Builder

**I turn real-world problems into working products and systems.**

Hansung University · Computer Engineering

<br/>

<a href="mailto:jkm0831123@gmail.com">
<img src="https://img.shields.io/badge/Email-jkm0831123%40gmail.com-111111?style=flat-square&logo=gmail&logoColor=white"/>
</a>

<a href="https://github.com/l1lsang">
<img src="https://img.shields.io/badge/GitHub-l1lsang-111111?style=flat-square&logo=github&logoColor=white"/>
</a>

</div>

---

## About

안녕하세요.  
**사용자가 실제로 사용할 수 있는 제품과 시스템을 만드는 Full-Stack Developer 장경민입니다.**

React와 TypeScript를 활용한 프론트엔드부터  
Spring Boot 기반 REST API, PostgreSQL 데이터베이스, Docker 환경 구성, AWS 배포까지  
**하나의 서비스를 처음부터 끝까지 직접 구축하는 것**에 관심이 있습니다.

현재 메인 프로젝트인 **Hansung Space**에서는 대학 공간 예약이라는 실제 문제를 해결하기 위해

**Frontend → Backend → Database → Cloud → IoT**

로 이어지는 전체 시스템을 설계하고 구현하고 있습니다.

또한 AI, 지도 기반 서비스, 실시간 시스템, IoT 등  
소프트웨어가 현실의 문제와 연결되는 영역을 적극적으로 탐구하고 있습니다.

```ts
const focus = [
  "Full-Stack Engineering",
  "Product Development",
  "System Architecture",
  "Cloud & Infrastructure",
  "Realtime & IoT Systems",
  "AI-powered UX"
];
```

> **Build things people can actually use.**

---

# Selected Projects

## Hansung Space · Smart Space Reservation Platform

**대학 공간 예약과 실제 공간 사용 상태를 연결하는 스마트 공간 관리 플랫폼**

대학교의 강의실과 스터디 공간을 조회하고 예약할 수 있으며,  
예약 데이터뿐만 아니라 센서를 이용한 **실제 공간 점유 상태까지 확인할 수 있도록 설계한 Full-Stack × Cloud × IoT 프로젝트**입니다.

현재 가장 집중해서 개발하고 있는 프로젝트입니다.

### Problem

기존 공간 예약 시스템에서는 공간이 `예약됨`으로 표시되어 있어도  
실제로 사용자가 공간을 이용하고 있는지는 알 수 없습니다.

반대로 예약되지 않은 공간이라도  
실제로 누군가 사용하고 있을 수 있습니다.

또한 실제 서비스에서는 단순한 예약 UI뿐 아니라

- 사용자 인증
- 공간 관리
- 예약 관리
- 데이터베이스
- 서버
- 배포
- 실시간 상태 관리

등 여러 시스템이 함께 동작해야 합니다.

### Solution

Hansung Space는 예약 정보와 실제 공간의 상태를 하나의 시스템으로 연결합니다.

```text
User
 │
 ▼
React + TypeScript
 │
 │ REST API
 ▼
Spring Boot
 │
 ▼
PostgreSQL
```

실제 공간에서는

```text
ESP32
 │
 ▼
mmWave Sensor
 │
 ▼
Occupancy Data
 │
 ▼
Backend
```

구조를 통해 공간의 실제 점유 상태를 전달합니다.

사용자는 하나의 서비스에서

```text
Reservation Status
        +
Realtime Occupancy
```

를 함께 확인할 수 있습니다.

---

### System Architecture

```text
                User
                  │
                  ▼
        React + TypeScript
              Vercel
                  │
                  │ HTTPS
                  ▼
        Spring Boot REST API
               AWS EC2
                  │
                  ▼
             PostgreSQL
```

IoT 데이터 및 연산량이 큰 기능은  
API 서버와 분리하여 처리할 수 있도록 확장 가능한 구조를 설계하고 있습니다.

```text
ESP32 / Sensors
       │
       ▼
 IoT Data Pipeline
       │
       ▼
 Spring Boot API
```

향후에는 별도의 Worker를 활용하여

```text
API
 │
 ▼
Message Queue
 │
 ▼
Optimization Worker
```

형태의 비동기 처리 구조로 확장할 계획입니다.

---

### Key Features

- 공간 목록 및 상세 조회
- 예약 가능 공간 검색
- 날짜 및 시간 기반 예약
- 사용자 인증
- 사용자별 예약 관리
- 공간별 예약 상태 관리
- REST API 기반 Frontend / Backend 분리
- PostgreSQL 기반 데이터 관리
- 센서 기반 실제 공간 점유 상태 감지
- ESP32 / mmWave Sensor 연동
- 관리자 공간 관리
- Cloud deployment
- 지도 및 위치 기반 공간 탐색
- 비동기 작업 처리 구조 설계
- Optimization Worker 구조 설계

---

### Infrastructure

Frontend와 Backend를 독립적으로 배포합니다.

```text
Frontend
Vercel
   │
   │ HTTPS
   ▼
hsp-api.gomindiscord.com
   │
   ▼
AWS EC2
   │
Spring Boot
   │
PostgreSQL
```

Backend 개발 환경은 Docker를 활용하여  
로컬 개발 환경과 서버 환경의 차이를 최소화하도록 구성했습니다.

---

### Engineering Challenges

#### 01. Frontend / Backend Separation

초기 단순 프론트엔드 구조에서 벗어나  
Spring Boot 기반 REST API 서버를 독립적으로 구축했습니다.

```text
Frontend
   │
REST API
   │
Backend
   │
Database
```

각 계층의 역할을 나누고  
실제 웹 서비스와 유사한 구조를 경험하고 있습니다.

---

#### 02. Database Architecture

PostgreSQL을 활용하여

- 사용자
- 공간
- 예약
- 시간
- 상태

데이터 사이의 관계를 정의하고 관리합니다.

단순한 NoSQL 기반 프로토타입을 넘어  
관계형 데이터베이스를 기반으로 서비스 데이터를 설계하고 있습니다.

---

#### 03. Docker Environment

PostgreSQL 및 Backend 환경을 Docker 기반으로 구성하여

```text
Local Development
        ≈
Server Environment
```

에 가까운 환경을 만들고 있습니다.

이를 통해 환경 차이로 발생하는 문제를 줄이고  
배포 가능한 애플리케이션 구조를 경험하고 있습니다.

---

#### 04. Cloud Deployment

Frontend는 **Vercel**,  
Backend는 **AWS EC2** 환경에 배포합니다.

Domain / HTTPS / API 통신 / CORS 설정까지 직접 구성하면서  
로컬 개발 환경을 실제 서비스 환경으로 확장하고 있습니다.

---

#### 05. Realtime Physical State

예약 데이터만으로는 실제 공간 상태를 알 수 없다는 문제를 해결하기 위해

**ESP32 + mmWave Sensor**

를 이용하여 현실 공간의 데이터를 웹 서비스와 연결하는 구조를 설계했습니다.

---

#### 06. Scalability

향후 다음과 같은 기능을 추가할 계획입니다.

- 최적 공간 추천
- 사용자 위치 기반 공간 탐색
- 길찾기
- 대중교통 정보
- 여러 사용자 위치 기반 중간 지점 계산
- 비동기 연산
- 캐싱

연산량이 많은 기능은 API 서버와 분리하여  
별도의 **Optimization Worker**에서 처리할 수 있도록 시스템을 설계하고 있습니다.

---

### My Contribution

- Product planning
- UX / reservation flow design
- Frontend development
- React application architecture
- REST API integration
- Spring Boot backend development
- PostgreSQL database design
- Docker development environment
- AWS EC2 deployment
- Vercel deployment
- Domain / HTTPS configuration
- Authentication architecture
- Web / IoT system architecture
- ESP32 sensor integration
- Async architecture design
- Optimization Worker architecture

---

### Stack

`React` `TypeScript`

`Spring Boot` `Java`

`PostgreSQL`

`Docker`

`AWS EC2` `Vercel`

`ESP32` `mmWave Sensor`

`REST API` `IoT`

**Status — Active Development**

[View Repository](https://github.com/l1lsang/hansung-place-system )

---

## 귀차나 · AI Life Assistant

**흩어진 생활 정보를 사용자가 해야 할 행동으로 바꾸는 AI 생활 관리 서비스**

스크린샷, 링크, 문자, 공지와 같이 일상에서 들어오는 정보를  
AI가 분석하여 **일정, 신청, 결제, 준비사항 등의 Action Card로 구조화**하고 완료까지 관리합니다.

### Product Flow

```text
Inbox
 ↓
AI Analysis
 ↓
Action Card
 ↓
User Review
 ↓
Action / Reminder
 ↓
Done / Archive
```

### My Contribution

- Product concept
- Service planning
- UX / interaction design
- Mobile frontend architecture
- AI interaction design
- Authentication / onboarding flow

### Stack

`Expo` `React Native` `TypeScript`

`Firebase` `Generative AI`

**Status — In Development**

---

## Spotit · Location-based Social Platform

**장소를 검색하는 지도가 아니라, 경험을 기록하는 지도**

사용자가 다녀온 장소를 지도 위에 사진과 함께 기록하고  
친구의 실제 방문 기록을 통해 새로운 장소를 발견할 수 있도록 설계한 지도 기반 SNS입니다.

### Key Features

- 지도 기반 장소 기록
- 장소 검색
- 사진 / 위치 기반 콘텐츠
- Custom Map Pin
- Authentication
- Firestore / Storage
- Mobile / Web UI

### Stack

`React` `TypeScript`

`Expo` `React Native`

`Firebase`

`Google Maps Platform`

`Vercel`

**Status — MVP Completed**

[View Repository](https://github.com/l1lsang/spotit)

---

## Flow · AI Flower & Gift Experience

**감정과 관계를 입력하면 선물의 형태까지 만들어주는 AI 기반 꽃·선물 서비스**

관계, 기억, 감정, 전달하고 싶은 분위기를 입력하면  
AI가 꽃 구성, 메시지, 이미지와 선물 방향을 제안합니다.

### Stack

`JavaScript`

`Web`

`Generative AI`

**Status — Prototype**

---

# Earlier Work

### Dream Defenders

Unity와 C#을 이용해 제작한 게임 프로젝트입니다.

플레이어 / 적 전투 시스템, 게임 상태 관리, UI 및 객체 간 상호작용을 구현했습니다.

`Unity` `C#` `Game Development`

---

### Discord Economy Platform

Discord 안에서 가상 화폐, 주식, 미니게임을 이용할 수 있도록 만든 경제 게임 시스템입니다.

Discord API와 Firebase를 이용해  
서버 내부에서 하나의 작은 온라인 서비스처럼 동작하도록 구현했습니다.

`Node.js` `Discord.js` `Firebase`

[View Repository](https://github.com/l1lsang/ganade)

---

# Tech Stack

<div align="center">

### Frontend

<img src="https://skillicons.dev/icons?i=react,ts,js,html,css&perline=8"/>

<br/>

`React` · `React Native` · `Expo` · `TypeScript` · `JavaScript`

---

### Backend

<img src="https://skillicons.dev/icons?i=spring,nodejs,java&perline=8"/>

<br/>

`Spring Boot` · `Node.js` · `REST API`

---

### Database & Realtime

<img src="https://skillicons.dev/icons?i=postgres,firebase&perline=8"/>

<br/>

`PostgreSQL` · `Firebase` · `Firestore`

---

### Cloud & DevOps

<img src="https://skillicons.dev/icons?i=aws,docker,vercel,linux,git,github&perline=8"/>

<br/>

`AWS EC2` · `Docker` · `Vercel` · `Linux`

`Git` · `GitHub`

---

### Programming Languages

<img src="https://skillicons.dev/icons?i=java,ts,js,c,cpp,python,cs&perline=8"/>

<br/>

`Java` · `TypeScript` · `JavaScript`

`C` · `C++` · `Python` · `C#`

---

### Mobile & IoT

<img src="https://skillicons.dev/icons?i=react,arduino&perline=8"/>

<br/>

`React Native` · `Expo`

`ESP32` · `mmWave Sensor` · `IoT`

---

### Game & Interactive

<img src="https://skillicons.dev/icons?i=unity,unreal&perline=8"/>

<br/>

`Unity` · `Unreal Engine`

---

### Design & Tools

<img src="https://skillicons.dev/icons?i=figma,vscode,idea&perline=8"/>

<br/>

`Figma` · `VS Code` · `IntelliJ IDEA`

</div>

---

# Engineering Interests

특정 프레임워크 자체보다  
**기술을 이용해 실제 문제를 해결하고 하나의 시스템으로 만드는 과정**에 관심이 있습니다.

| Area | Focus |
|---|---|
| Full-Stack | Frontend ↔ Backend ↔ Database |
| Frontend | React, TypeScript, React Native |
| Backend | Spring Boot, REST API, Node.js |
| Database | PostgreSQL, Firebase |
| Cloud | AWS, Docker, Vercel |
| Architecture | API, Worker, Async Processing |
| AI | AI-powered UX, Automation |
| Realtime | Realtime synchronization |
| Location | Maps, location-based services |
| Embedded | ESP32, Sensors, IoT |
| Research | Algorithms, Computational Mathematics |

---

# How I Build

### 01. Understand the problem

기능부터 구현하기보다  
**왜 이 기능이 필요한지 먼저 정의합니다.**

---

### 02. Design the system

사용자 화면뿐만 아니라

```text
Frontend
Backend
Database
Infrastructure
```

가 어떻게 연결될지 함께 고민합니다.

---

### 03. Build the smallest working product

완벽한 설계부터 시작하기보다  
**실제로 동작하는 MVP를 빠르게 구현합니다.**

---

### 04. Deploy it

로컬에서 실행되는 코드에서 끝내지 않고  
실제 사용자가 접근할 수 있는 환경까지 배포하는 것을 중요하게 생각합니다.

---

### 05. Learn from failure

오류를 단순히 수정하는 것에서 끝내지 않고  
왜 발생했는지 이해하고 다음 시스템 설계에 반영합니다.

---

# Beyond Full-Stack

Full-Stack 개발을 중심으로 하고 있지만  
제품 전체를 이해하기 위해 다양한 영역을 경험하고 있습니다.

- Web Application
- Mobile Application
- Backend API
- Relational Database
- Cloud Infrastructure
- Docker
- AI-powered Products
- Embedded Systems
- IoT
- Game Development
- C / C++ & Data Structures
- Computational Mathematics

이를 통해 단순히 화면이나 API 하나를 구현하는 개발자를 넘어

**사용자가 보는 화면부터 서버, 데이터베이스, 인프라, 현실의 센서까지 연결할 수 있는 개발자**

로 성장하고 있습니다.

---

<div align="center">

## `quokka@github:~$ build_something_useful_`

**Full-Stack Developer · Product Builder**

아이디어를 코드로,  
코드를 시스템으로,  
시스템을 사람들이 사용할 수 있는 제품으로.

<br/>

<a href="mailto:jkm0831123@gmail.com">
<img src="https://img.shields.io/badge/Contact-jkm0831123%40gmail.com-111111?style=for-the-badge&logo=gmail&logoColor=white"/>
</a>

</div>
