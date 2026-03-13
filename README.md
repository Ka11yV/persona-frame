# 🤖 Persona Frame

> **"퍼비야"** — 액자 속에 살아있는 AI 어시스턴트

일상 공간에 자연스럽게 녹아드는 **액자형 AI 대시보드**입니다.  
시간, 날씨, 일정을 항상 표시하며, 음성 호출 한 마디로 AI와 대화할 수 있습니다.

---

## ✨ 주요 기능

### 📊 기본 대시보드 (항상 표시)
- 현재 **시간** 실시간 표시
- 현재 **날씨** 정보 표시
- **오늘 일정** 표시

### 🎙 AI 인터랙션
| 기능 | 설명 |
|------|------|
| Wake Word 감지 | "퍼비야" 호출로 AI 활성화 |
| 음성 일정 관리 | 음성으로 일정 추가 / 삭제 / 조회 |
| 음악 재생 | 음성 명령으로 음악 제어 |
| 타이머 | 공부 타이머, 일반 타이머 설정 |
| 하루 일과 회고 | 당일 일정을 AI가 요약해서 카드로 제공 |
| 맞춤 의사결정 도움 | 날씨·위치 데이터 기반 AI 추천 카드 |
| 즐겨찾기 | 자주 하는 질문/명령을 저장해 빠르게 실행 |

### 🌿 환경 반응형
| 기능 | 설명 |
|------|------|
| 절전 모드 | 1시간 움직임 없으면 화면 Sleep |
| 날씨/시간 연동 배경 | 날씨·시간에 따라 배경 자동 변경 |
| 캐릭터 상태 변화 | idle / listening / thinking / sleep |
| 진동 감지 호출 | 액자 프레임을 톡톡 두드려 AI 호출 (무음 모드) |

---

## 🛠 기술 스택

### Frontend
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Framer Motion](https://img.shields.io/badge/Framer_Motion-0055FF?style=flat-square&logo=framer&logoColor=white)

### AI / 음성 인식
![OpenAI](https://img.shields.io/badge/Whisper-412991?style=flat-square&logo=openai&logoColor=white)
- Porcupine (Wake Word 감지)
- Web Speech API

### 외부 API
- OpenWeatherMap API / 기상청 API (날씨)
- Google Calendar API (일정 연동)
- Claude API / GPT API (AI 인터랙션)

---

## 🗂 프로젝트 구조

```
persona-frame/
├── src/
│   ├── components/
│   │   ├── widgets/          # 시간, 날씨, 일정 위젯
│   │   ├── character/        # 퍼비 캐릭터 & 애니메이션
│   │   └── cards/            # AI 응답 카드
│   ├── hooks/
│   │   ├── useWakeWord.ts    # Wake word 감지
│   │   ├── useSpeech.ts      # 음성 인식
│   │   └── useWeather.ts     # 날씨 데이터
│   ├── store/                # 전역 상태 관리 (Zustand)
│   └── api/                  # 외부 API 연동
├── public/
│   └── backgrounds/          # 날씨/시간별 배경 이미지
└── README.md
```

---

## 🚀 시작하기

### 사전 준비
- Node.js 18+
- npm 또는 yarn

### 설치

```bash
git clone https://github.com/Ka11yV/persona-frame.git
cd persona-frame
npm install
```

### 환경변수 설정

`.env` 파일을 생성하고 아래 값을 입력하세요:

```env
VITE_OPENWEATHER_API_KEY=your_openweather_api_key
VITE_CLAUDE_API_KEY=your_claude_api_key
VITE_GOOGLE_CALENDAR_CLIENT_ID=your_google_client_id
```

### 실행

```bash
npm run dev
```

---

## 📅 개발 현황

- [x] 프로젝트 기획 및 ERD 설계
- [ ] 기본 대시보드 UI (시간/날씨/일정)
- [ ] 캐릭터 애니메이션 (idle/listening/thinking/sleep)
- [ ] Wake Word 감지 ("퍼비야")
- [ ] 음성 명령 처리
- [ ] AI 인터랙션 (의사결정 도움, 회고)
- [ ] 즐겨찾기 기능
- [ ] 진동 감지 호출
- [ ] 절전 모드

---

## 👥 팀원

| 이름 | 역할 |
|------|------|
| Ka11yV | - |
| msnoeuan | - |
| 엘리자베스 1세 | - |

---

## 📄 라이선스

This project is licensed under the MIT License.
