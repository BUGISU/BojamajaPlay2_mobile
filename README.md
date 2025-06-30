# 🎮 보자마자 PLAY 2 모바일 (BOJAMAJA PLAY 2 MOBILE)

![Hero](https://github.com/JISUSAMA/JISUSAMA/assets/38304918/1029c970-2843-423a-9a63-e88606b62bee)

**멀티 미니게임 아케이드 플랫폼**  
10종 이상의 캐주얼 게임을 하나의 모바일 앱에 통합하고, 랭킹 시스템·광고·인앱 결제·상점 등을 연동해 완성도 높은 오프라인–온라인 하이브리드 모바일 콘텐츠로 구현한 프로젝트입니다.

---

## 📅 개발 기간
**2020.11 ~ 2021.06 (8개월)**

---

## 🛠️ 기술 스택
- Unity 3D (URP 미사용)
- C#
- Android Build Support
- Google AdMob
- In-App Purchase (IAP)
- Local + Remote Ranking System (JSON 기반)

## 💻 주요 기술 스택 상세

| 분류           | 기술                       | 설명                                   |
| ------------ | ------------------------ | ------------------------------------ |
| **게임 엔진**    | Unity3D                  | URP 미사용, 경량화된 2D/3D 게임 개발 환경         |
| **프로그래밍 언어** | C#                       | 전반적인 게임 로직, UI 제어, 서버 통신 처리          |
| **빌드 대상**    | Android                  | Google Play 및 APK 기반 배포              |
| **광고 연동**    | Google AdMob             | 보상형 광고 (Rewarded Ads), 전면 광고 포함      |
| **인앱 결제**    | Unity IAP                | 다이아몬드 구매 기능, IAPManager로 중앙 제어       |
| **서버 연동**    | JSON 통신 기반 랭킹 서버         | `UnityWebRequest`를 활용한 서버 간 랭킹 등록/조회 |
| **UI 애니메이션** | DOTween                  | 버튼 클릭, 슬라이더, 패널 전환 등 UI 연출 강화        |
| **데이터 저장**   | PlayerPrefs              | 로컬 유저 정보 저장 (닉네임, 최고점 등)             |
| **씬 전환 관리**  | SceneManager + 커스텀 분기    | 모드/게임 간 흐름 관리                        |
| **오디오 관리**   | AudioSource + Manager 패턴 | 효과음 및 BGM 통합 제어                      |

## 🔧 주요 기술 세부 설명

| 범주            | 기술 / 구성 요소                                                 | 설명                                                     |
| ------------- | ---------------------------------------------------------- | ------------------------------------------------------ |
| **게임 엔진**     | Unity 3D                                                   | URP 미사용, 경량 구성으로 모바일 최적화 중심 개발. 10개 미니게임 씬 통합 구조로 구성.  |
| **프로그래밍 언어**  | C#                                                         | 게임 로직, 상태 관리, UI 전환, 서버 통신, 광고/IAP 로직 등 전체 로직 설계 및 구현. |
| **게임 모드**     | `ClassicMod.cs`, `ModPlayCheck.cs`                         | 사용자 선택에 따라 단일 게임 or 10개 연속 게임 플레이 분기 구현.               |
| **UI 시스템**    | Unity UI + DOTween                                         | 랭킹 등록, 점수 표시, 튜토리얼 안내, 상점, 게임 결과 등 애니메이션 포함 전체 UI 구축.  |
| **광고 연동**     | Google AdMob (`AdManager.cs`)                              | 보상형 광고 및 배너 광고 삽입. 광고 성공 시 재화 보상 지급 연동.                |
| **인앱 결제**     | Unity IAP (`IAPManager.cs`)                                | 다이아몬드 패키지 구매 기능 포함. 상점 내 UI 및 구매 응답 처리.                |
| **상점 시스템**    | `ShopAppManager.cs`                                        | 다이아몬드 화폐 사용 및 광고 시청/결제 보상 수령 처리.                       |
| **랭킹 시스템**    | JSON 서버 통신 (`ServerManager.cs`, `MyRankingManager.cs`)     | 사용자 점수 등록 및 랭킹 Top20 조회 가능. 서버와 비동기 통신 처리.             |
| **데이터 저장**    | `PlayerPrefs`                                              | 닉네임, 최고 점수, 다이아 수량, 설정값 등 로컬 데이터 저장.                   |
| **게임 전환 흐름**  | `SceneManager` + 커스텀 씬 리스트                                 | 다음 게임 자동 전환, 결과 씬 이동, 모드 별 분기 처리.                      |
| **QA 및 유지보수** | `ScoreManager.cs`, `PlayerController.cs`, `UIManager.cs` 등 | 각 게임 씬 별로 점수/이벤트 로직 정비 및 UI 오류 수정 등 전면 QA 수행.          |
| **애니메이션 효과**  | DOTween                                                    | UI 트랜지션, 별점 표시, 효과음 타이밍 연동 등 부드러운 사용자 경험 제공.           |
| **사운드 관리**    | `AudioSource` + BGM/SFX                                    | `SoundManager.cs` 통해 효과음 및 배경음 통합 관리 및 일관성 유지.         |

---

## ⚙️ 핵심 기능 요약

| 항목 | 설명 |
|------|------|
| 🎮 **게임 통합 시스템** | 10종 게임 통합 및 씬 관리 시스템 구축 |
| 🧩 **클래식 / 랭킹 모드** | 게임 플레이 모드 분기 및 UI 구성 |
| 🛍 **상점 + 아이템 시스템** | 다이아몬드 화폐, 광고 리워드, IAP 적용 |
| 🏆 **랭킹 시스템** | 서버 기반 점수 기록 및 Top 20 UI 표시 |
| 🎨 **UI 리뉴얼** | 시즌 1 대비 전면 리디자인 적용 |
| 🧪 **QA 및 버그 수정** | 인수 이후 모든 씬에 대한 안정화 수행 |

---

## 🗂 프로젝트 구조 (일부)

```

Scripts/
├── Start/               # 앱 시작 및 모드 관리
├── Classic/             # 클래식 모드 점수 로직
├── Ranking/             # 랭킹 UI 및 서버 통신
├── Shop/                # 광고·IAP·상점 시스템
├── Server/              # 닉네임 검색, 점수 등록 등
└── Pirates/, Zombie/, Bowling/, Soccer/, Hotpot/, …

```

---

## 🔧 주요 기여 작업
- **게임 10종 통합** 및 중앙 흐름(`MainAppManager`, `ModPlayCheck`) 설계  
- **QA / 버그 수정**: `PlayerController`, `UIManager`, `ScoreManager` 안정화  
- **UI 전면 리뉴얼**: 다크 테마, 모드 선택·상점·랭킹 화면 개편  
- **모드 분기 시스템**: `ClassicMod.cs` 로 점수/보상 로직 분리  
- **광고·상점 연동**: `AdManager`, `IAPManager`, `ShopAppManager` 구현  
- **랭킹 서버 연동**: `ServerManager`, `MyRankingManager` 등으로 JSON 통신  

---

## 🖼 인게임 이미지

| | |
|:-:|:-:|
| ![](https://github.com/JISUSAMA/JISUSAMA/assets/38304918/c24ea6f3-732b-47f4-9422-8b261d51c44e) | ![](https://github.com/JISUSAMA/JISUSAMA/assets/38304918/fcbfae14-4fbd-4dee-9fb1-f8ab9bc30fb9) |
| ![](https://github.com/JISUSAMA/JISUSAMA/assets/38304918/60285ecb-d833-4c6d-bd34-2adaee5fff54) | ![](https://github.com/JISUSAMA/JISUSAMA/assets/38304918/d709ef07-7d98-440e-b9ae-62e41e04dc38) |

---
## 🖼 UI 리뉴얼 작업
### 🔻 Before
<img src="https://github.com/JISUSAMA/JISUSAMA/assets/38304918/a4de3e3c-96cf-4ce1-8f18-5ea2d8008323">

### 🔻 After (Classic / Ranking 모드 UI)
<p align="center">
  <img src="https://github.com/JISUSAMA/JISUSAMA/assets/38304918/f5522ad6-b4b6-4594-92c9-ffb2ec29ec3c" width="49%">
  <img src="https://github.com/JISUSAMA/JISUSAMA/assets/38304918/db902469-808c-4c83-b6e8-d45fe78565b9" width="49%">

---

## 🛒 상점 & 광고 UI

| |
|:-:|
| ![](https://github.com/JISUSAMA/JISUSAMA/assets/38304918/72fbe959-2dea-4efb-987c-cf7e2e4799d0) |

---

## 🏆 랭킹 시스템 화면

| | |
|:-:|:-:|
| ![](https://github.com/JISUSAMA/JISUSAMA/assets/38304918/702fbd81-0cef-4601-9bc5-7a75e32e7e8c) | ![](https://github.com/JISUSAMA/JISUSAMA/assets/38304918/7bef9da9-467b-47f6-8eb4-974ca84f0445) |

---

## ▶️ 유튜브 홍보 영상

| 영상 1 | 영상 2 |
|:--:|:--:|
| [![Video](http://img.youtube.com/vi/P1kxqV_Yfwg/0.jpg)](https://www.youtube.com/watch?v=P1kxqV_Yfwg) | [![Video](http://img.youtube.com/vi/j06lBQHTU0o/0.jpg)](https://www.youtube.com/watch?v=j06lBQHTU0o) |
