<div align="center">

<img src="https://github.com/l1lsang.png" width="96" style="border-radius:50%"/>

# Jang Gyeongmin

### Frontend Developer · Product Builder

**I turn ideas and everyday problems into working products.**

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

안녕하세요. **사람이 실제로 사용할 수 있는 서비스를 만드는 개발자 장경민입니다.**

React와 TypeScript를 중심으로 웹과 모바일 서비스를 만들고 있으며,  
아이디어를 화면으로 구현하는 것뿐만 아니라 **문제 정의, 사용자 흐름, 데이터 구조, 배포까지 제품 전체를 이해하며 개발하는 것**에 관심이 있습니다.

최근에는 **AI, 지도 기반 서비스, 실시간 데이터, IoT**를 실제 제품 경험과 연결하는 프로젝트를 만들고 있습니다.

```ts
const focus = [
  "Frontend Engineering",
  "Product Development",
  "AI-powered UX",
  "Web & Mobile",
  "Realtime Systems"
];
```

> **Build things people can actually use.**

---

# Selected Projects

## 귀차나 · AI Life Assistant

**흩어진 생활 정보를 사용자가 해야 할 행동으로 바꾸는 AI 생활 관리 서비스**

스크린샷, 링크, 문자, 공지와 같이 일상에서 들어오는 정보를  
단순히 저장하는 것이 아니라 AI가 분석하여 **일정, 신청, 결제, 준비사항 등의 Action Card로 구조화**하고 완료까지 관리합니다.

### Problem

기존 캘린더와 할 일 앱은 사용자가 직접 내용을 정리하고 입력해야 합니다.

하지만 정작 일정 관리가 어려운 사용자는  
**정보를 정리해서 캘린더에 입력하는 과정 자체를 하지 않는 경우가 많습니다.**

### Product Flow

`Inbox`

→ `AI Analysis`

→ `Action Card`

→ `User Review`

→ `Action / Reminder`

→ `Done or Archive`

### My Contribution

- Product concept & service planning
- UX / interaction flow design
- Mobile frontend architecture
- AI interaction design
- Inbox / Action / Chat / Archive 구조 설계
- Authentication, onboarding, subscription flow 설계

### Stack

`Expo` `React Native` `TypeScript` `Firebase` `Generative AI`

**Status — In Development**

---

## Spotit · Location-based Social Platform

**장소를 검색하는 지도가 아니라, 경험을 기록하는 지도**

사용자가 다녀온 장소를 지도 위에 사진과 함께 기록하고,  
친구의 실제 방문 기록을 통해 새로운 장소를 발견할 수 있도록 설계한 **지도 기반 기록 SNS**입니다.

### Problem

기존 지도 서비스는 장소 검색에 집중되어 있고,  
SNS의 장소 기록은 시간순 피드에 묻히기 쉽습니다.

Spotit은 사용자의 경험을 **위치 자체를 중심으로 다시 탐색할 수 있도록** 설계했습니다.

### Key Features

- 지도 기반 장소 기록 및 탐색
- 사진과 위치를 결합한 사용자 콘텐츠
- Custom map pin
- Authentication
- Firestore / Storage 기반 데이터 관리
- 장소 검색 및 지도 인터랙션
- Responsive Web / Mobile UI

### My Contribution

- Product planning
- Frontend development
- UI / UX design
- Firebase data architecture
- Google Maps integration
- Authentication & Storage
- Deployment

### Stack

`React` `TypeScript` `Expo` `React Native`  
`Firebase` `Google Maps Platform` `Vercel`

**Status — MVP Completed**

[View Repository](https://github.com/l1lsang/spotit)

---

## Hansung Space · Smart Space Reservation

**예약 정보와 실제 공간 사용 상태를 연결하는 스마트 공간 관리 시스템**

한성대학교 공간 예약 시스템을 기반으로,  
단순히 예약 여부만 보여주는 것을 넘어 **실제 공간에 사람이 있는지 센서를 통해 확인할 수 있도록 설계한 Web × IoT 프로젝트**입니다.

### Problem

예약 시스템에서는 공간이 `예약됨`으로 표시되어도  
실제로 사용 중인지 알기 어렵습니다.

반대로 예약되지 않았지만 실제로 사용 중인 공간이 존재할 수도 있습니다.

### Solution

예약 데이터와 센서 데이터를 결합하여

`Reservation Status`

+

`Realtime Occupancy`

를 동시에 확인할 수 있도록 구성했습니다.

### Key Features

- 공간별 예약 가능 시간 조회
- 실시간 예약 상태 동기화
- 센서 기반 실제 점유 상태 감지
- 관리자 공간 현황 확인
- Web ↔ Firebase ↔ IoT 데이터 연결

### My Contribution

- Reservation UX design
- Frontend development
- Firebase realtime architecture
- Web / IoT system architecture
- ESP32 sensor integration design

### Stack

`React` `TypeScript` `Firebase`  
`ESP32` `mmWave Sensor` `IoT`

**Status — In Development**

[View Repository](https://github.com/l1lsang/hsp)

---

## Flow · AI Flower & Gift Experience

**감정과 관계를 입력하면 선물의 형태까지 함께 만들어주는 AI 기반 꽃·선물 서비스**

단순히 꽃 상품을 검색하는 방식에서 벗어나  
받는 사람과의 관계, 기억, 감정, 전달하고 싶은 분위기 등을 기반으로  
AI가 **꽃 구성, 메시지, 이미지와 선물 방향을 제안하는 서비스**입니다.

### Input

`Recipient`

`Memory`

`Emotion`

`Tone`

`Style`

`Budget`

↓

### AI Experience

`Flower Concept`

`Message`

`Visual`

`Gift Direction`

### My Contribution

- Service concept
- AI-based product UX
- User input flow
- Web prototype development
- Generative experience design

### Stack

`JavaScript` `Web` `Generative AI`

**Status — Prototype**

---

# Earlier Work

### Dream Defenders

Unity와 C#을 이용해 제작한 게임 프로젝트입니다.  
플레이어/적 전투 시스템, 게임 상태 관리, UI 및 객체 간 상호작용을 구현했습니다.

`Unity` `C#` `Game Development`

---

### Discord Economy Platform

Discord 안에서 가상 화폐와 주식, 미니게임을 사용할 수 있도록 만든 경제 게임 시스템입니다.

사용자 데이터와 게임 상태를 Firebase에 저장하고  
Discord API와 연결하여 서버 안에서 하나의 작은 서비스처럼 동작하도록 구현했습니다.

`Node.js` `Discord.js` `Firebase`

[View Repository](https://github.com/l1lsang/ganade)

---

# Core Stack

<div align="center">

### Frontend

<img src="https://skillicons.dev/icons?i=react,ts,js,html,css&perline=5"/>

<br/>

`React` · `React Native` · `Expo` · `TypeScript`

<br/><br/>

### Backend & Platform

<img src="https://skillicons.dev/icons?i=nodejs,firebase,vercel&perline=5"/>

<br/>

`Node.js` · `Firebase` · `Firestore` · `Vercel`

<br/><br/>

### Programming

<img src="https://skillicons.dev/icons?i=c,cpp,python,java,cs&perline=5"/>

<br/><br/>

### Other Engineering

<img src="https://skillicons.dev/icons?i=unity,unreal,arduino,git,github,figma&perline=6"/>

</div>

---

# Engineering Interests

제가 관심 있는 것은 특정 프레임워크 하나보다  
**기술을 이용해 실제 문제를 해결하는 과정**입니다.

| Area | Focus |
|---|---|
| Frontend | React, TypeScript, React Native |
| Product | UX Flow, Interaction, Product Architecture |
| AI | AI-powered UX, Automation, Generative Interfaces |
| Realtime | Firebase, realtime synchronization |
| Location | Maps, location-based services |
| Embedded | ESP32, Sensors, IoT |
| Research | Algorithms, Computational Mathematics |

---

# How I Build

### 01. Understand the problem

기능부터 만들기보다  
**왜 이 기능이 필요한지 먼저 정의합니다.**

### 02. Design the flow

사용자가 서비스를 처음 만나는 순간부터  
목표를 완료하는 순간까지의 흐름을 설계합니다.

### 03. Build the smallest working product

완벽한 설계보다  
**실제로 동작하는 MVP를 빠르게 구현합니다.**

### 04. Learn from failure

오류를 단순히 수정하는 데서 끝내지 않고  
왜 발생했는지 이해하고 다음 구조에 반영합니다.

---

# Beyond Frontend

프론트엔드를 중심으로 개발하고 있지만  
제품 전체를 이해하기 위해 다양한 분야를 직접 경험하고 있습니다.

- Web & Mobile Application
- Firebase architecture
- AI-powered products
- Embedded systems with ESP32
- Unity / Unreal Engine
- C / C++ & Data Structures
- Computational mathematics experiments

이를 통해 화면을 구현하는 개발자를 넘어  
**제품의 전체 구조와 사용자 경험을 함께 이해할 수 있는 개발자**로 성장하고 있습니다.

---

<div align="center">

## `quokka@github:~$ build_something_useful_`

**Frontend Developer · Product Builder**

아이디어를 코드로,  
코드를 사람들이 사용할 수 있는 제품으로.

<br/>

<a href="mailto:jkm0831123@gmail.com">
<img src="https://img.shields.io/badge/Contact-jkm0831123%40gmail.com-111111?style=for-the-badge&logo=gmail&logoColor=white"/>
</a>

</div>
