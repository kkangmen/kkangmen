<div align="center">

# 김강민 &nbsp;|&nbsp; Back-end & DevOps

**측정하고, 줄이고, 자동화합니다.**

로그와 부하 테스트로 근거를 만든 뒤 개선하는 것을 좋아합니다.<br/>
불필요한 자원 낭비를 줄이고, 사람이 반복하던 일을 파이프라인으로 옮깁니다.

[![Email](https://img.shields.io/badge/pickofee@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:pickofee@gmail.com)
[![GitHub](https://img.shields.io/badge/kkangmen-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/kkangmen)

</div>

---

## About

- 홍익대학교 컴퓨터공학과 (2021.03 ~ 2027.02 졸업예정)
- **도메인을 먼저 이해하고 코드를 작성합니다.** ta4j, RAG 아키텍처처럼 낯선 기술은 개념을 정리한 뒤 적용합니다.
- **지표 없이 개선하지 않습니다.** MDC 로그와 Grafana k6로 전후를 같은 조건에서 측정합니다.
- **기준을 문서로 남깁니다.** 커밋 컨벤션과 PR 흐름을 정리해 팀에 공유합니다.

---

## Tech Stack

**Backend**

![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring%20Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)
![JPA](https://img.shields.io/badge/JPA%20/%20QueryDSL-59666C?style=flat-square&logo=hibernate&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

**Cloud & CI/CD**

![AWS](https://img.shields.io/badge/AWS%20EC2%20·%20RDS%20·%20S3-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)

**Monitoring & Testing**

![CloudWatch](https://img.shields.io/badge/CloudWatch-FF4F8B?style=flat-square&logo=amazoncloudwatch&logoColor=white)
![Grafana k6](https://img.shields.io/badge/Grafana%20k6-7D64FF?style=flat-square&logo=k6&logoColor=white)

---

## Projects

### [Fit-Me](https://github.com/FitMe-umc-10th/FitMe_back) &nbsp;·&nbsp; 대학생 맞춤형 장학금 · 공모전 추천 서비스

`2026.06 ~ 2026.08` &nbsp;|&nbsp; Backend 5명 &nbsp;|&nbsp; [배포](https://fit-me-front-smoky.vercel.app/)

| | |
|---|---|
| **1시간 → 쿼리 2회** | MDC 로깅 필터로 요청 단위 추적 체계를 만들어 장애 원인 분석 시간 단축 |
| **p95 12.12s → 0.74s** | 인증 메일 발송을 `@Async` 로 전환, Grafana k6 동시 요청 40건으로 검증 |
| **200줄 → 80줄** | QueryDSL 동적 쿼리로 재작성, Fetch Join 으로 N+1 방지 |

`OAuth2User` 와 `UserDetails` 를 함께 구현한 통합 인증 클래스 `PrincipalDetails` 를 설계해,
소셜·폼 로그인이 동일한 규격의 인증 객체를 반환하도록 정리했습니다.

<br/>

### [JUBY](https://github.com/JUBYInvest/JUBY-BE) &nbsp;·&nbsp; 주식 초보자를 위한 AI 투자 비서

`2026.03 ~ 진행중` &nbsp;|&nbsp; Backend 2명

| | |
|---|---|
| **AI 토큰 40% 절감** | 백테스팅 결과를 100점 만점 적합도 점수로 압축해 프롬프트 입력 최소화 |
| **4축 × 3지표** | 안정성 · 수익성 · 효율성 · 성장성을 정규화한 자체 퀀트스코어링 설계 |
| **5가지 매매 전략** | ta4j 기반 SMA · 볼린저 밴드 · RSI · 거래량 돌파 · MACD |

KIS API 와 네이버 뉴스 API 를 연동한 비동기 스케줄러를 운영합니다.
지수 백오프와 최대 3회 재시도, 누락분 보정 실행으로 데이터 정합성을 확보했습니다.

<br/>

### [ODDNARY](https://github.com/Caudex-Ne-O-rdinary/Caudex-Backend) &nbsp;·&nbsp; 괴근식물 수집가를 위한 공유 가상 정원

`무박 2일 해커톤` &nbsp;|&nbsp; Backend 2명

| | |
|---|---|
| **배포 1일 → 3분** | 기능보다 먼저 Docker 기반 CI/CD 파이프라인을 구축 |
| **S3 + RDS 분리** | 이미지는 S3, 메타데이터만 RDS 에 두어 API 응답과 이미지 트래픽 분리 |

PM · 디자이너 · iOS · Android 와 함께 이틀 만에 앱 하나를 완성했습니다.

---

## 학습 기록

새 기술은 쓰기 전에 개념을 정리합니다.

- [Spring Security & OAuth 2.0](https://fourth-value-7d5.notion.site/Spring-Security-OAuth2-0-31af03c7a0588055b245e7d376d635bd)
- [ta4j 백테스팅 라이브러리](https://fourth-value-7d5.notion.site/ta4j-320f03c7a05880b8ad5bdb24e9f2de82)
- [CI/CD](https://fourth-value-7d5.notion.site/CI-CD-32ef03c7a05880b19a35da1444e13986)
- [DevOps](https://fourth-value-7d5.notion.site/DevOps-31af03c7a058802a9014c30b3332feb4)

---

<div align="center">

![kkangmen's GitHub stats](https://github-readme-stats.vercel.app/api?username=kkangmen&show_icons=true&hide_border=true&theme=default)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=kkangmen&layout=compact&hide_border=true&theme=default)

</div>

[![Solved.ac Profile](http://mazassumnida.wtf/api/v2/generate_badge?boj=kkangmen)](https://solved.ac/kkangmen/)
