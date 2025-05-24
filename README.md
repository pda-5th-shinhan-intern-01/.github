
# 🔥 HOTSIGNAL

> **“경제지표 발표, 그냥 흘려보낼 건가요?”**  
> 경제지표 기반의 시장 반응을 **한눈에**, **정량적으로** 분석합니다.

<br/>

## 🎥 데모 영상 및 주요 화면

[HOTSignal 시연 영상](https://youtu.be/0jQyY5Yp7BM)  

| 메인 대시보드 | 경제지표 상세 |
|---------------|----------------|
| ![dashboard](https://github.com/user-attachments/assets/a76f647a-eaab-4e44-a213-4a20e1ecbdf0) | ![indicator](https://github.com/user-attachments/assets/69784569-8809-4568-826a-cc67ee86d524) |

| 민감도 히트맵 | FOMC 회의록 요약 |
|----------------|-----------------|
| ![heatmap](https://github.com/user-attachments/assets/f6e80270-b553-4802-a8e7-6d44bbbfb1a2) | ![fomc](https://github.com/user-attachments/assets/3621ce5f-45a1-477f-adf7-6587aac42b83) |

> 캘린더, 종목 상세, 트리맵, 차트 등 인터랙티브 UI로 구성되어 있습니다.

<br/>

## 📌 프로젝트 개요

**HOTSIGNAL**은 미국의 주요 경제지표 발표(CPI, FOMC 등)와 주식 시장의 반응을 분석하여 투자자에게 직관적인 인사이트를 제공합니다.

### 🎯 문제 인식
- 경제지표는 시장을 선도하는 신호지만 정보가 산재되어 있고, 비전문가에게는 접근성이 낮음
- 발표 전후 시장 반응을 통합적으로 보여주는 서비스 부족

### 💡 해결 방안
- 섹터/종목별 경제지표 민감도 분석
- 발표 이벤트 중심의 시계열 차트
- FOMC 키워드 비교 및 요약 제공

<br/>

## 🔍 주요 기능

- 📅 **경제지표 캘린더**: 예정된 발표 일정 및 수치 확인
- 🔥 **Hot Reactions**: 지표에 민감하게 반응한 종목 실시간 노출
- 📈 **종목 상세 페이지**: 민감도 그래프, 이벤트 주가 차트
- 📊 **히트맵 시각화**: 섹터별 지표 반응도 정량 시각화
- 🧠 **FOMC 요약**: 요약·비교 기능으로 회의 내용 빠른 파악

<br/>

## ⚙️ 기술 스택

| 분야       | 기술 |
|------------|------|
| Frontend   | React, TailwindCSS, Framer Motion |
| Backend    | Spring Boot, Java, JPA |
| ETL        | Python, MySQL, Redis |
| Infra      | Docker, NHN Cloud, GitHub Actions |
| DB         | MySQL (Master-Replica), Redis (예정) |
| 협업 도구  | GitHub, Notion |

<br/>

## ⚙️ 아키텍처 및 ERD

### 📑 아키텍처
![image](https://github.com/user-attachments/assets/749f2146-5bd2-40df-a18b-54540a3a6e7b)

### 📜 ERD
![image](https://github.com/user-attachments/assets/f888a9dd-b53b-4c9d-ba7b-69e09639aa05)


## 🧪 민감도 분석 로직

- **종목별**: OLS 회귀분석 → `예상 퍼포먼스 = β × Δ지표변화율`
- **섹터별**: 피어슨 상관계수 → 패턴 중심의 시각화
- Rolling 윈도우(3년) 기반으로 최신 민감도 반영

<br/>

## 🔧 고도화 계획

* ARIMAX 기반 시계열 예측 모델 적용
* 서버리스 기반 리포트 요약 연산 분리 (ex. Lambda)
* Redis 캐싱 도입으로 API 응답속도 3\~5배 향상 기대
* 주요 API 비동기 처리 구조 개선

<br/>

## 👥 팀 소개

| 이름  | 역할      | 담당 업무              |
| --- | ------- | ------------------ |
| 곽성은 | 프론트엔드   | 종목 상세 페이지, FOMC 수집 |
| 김동재 | 백엔드/인프라 | API 설계 및 인프라 구성    |
| 라수빈 | 프론트엔드   | 캘린더, 인트로 페이지       |
| 박고은 | 프론트엔드   | FOMC 요약 시각화        |
| 양일교 | 프론트엔드   | 히트맵, 섹터 페이지        |
| 하민지 | 백엔드     | 민감도 분석 및 히트맵 로직    |

<br/>


