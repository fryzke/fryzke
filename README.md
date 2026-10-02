<!-- 헤더 영역 -->
<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=auto&height=220&section=header&text=Hi%20there,%20I'm%20fryzke%20👋&fontSize=42&animation=fadeIn&fontAlignY=38" width="100%" />

  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=20&duration=3000&pause=1000&color=2563EB&center=true&vCenter=true&width=700&lines=신입+Java+%2F+Spring+백엔드+개발자;트래픽+최적화와+데이터+정합성을+고민합니다;이유+있는+코드로+비즈니스+가치를+만듭니다" alt="Typing SVG" />
  </a>
</div>

<br>

### 🧑‍💻 About Me
- 🎯 **탄탄한 Java/Spring 기본기와 문제 해결력을 바탕으로 이유 있는 코드를 작성하는 백엔드 개발자**입니다.
- ⚡ **성능 최적화**: N+1 쿼리 해결(응답속도 85% 개선), Redis ZSET 기반 실시간 집계(DB 부하 0건) 등 성능 병목을 수치로 개선한 경험이 있습니다.
- 🔒 **데이터 정합성 & 동시성**: 비관적 락(Pessimistic Lock)과 멱등성 설계를 통해 결제·포인트 동시 차감 실패율을 0%로 안정화했습니다.
- 🛠️ **클린 코드 & 아키텍처**: QueryDSL을 활용한 동적 검색 캡슐화, 단일 진실 공급원(SSOT) 설계로 변경에 유연한 시스템을 구축합니다.

---

### 🛠️ Tech Stacks

#### Backend & Data
<div align="left">
  <img src="https://img.shields.io/badge/Java_17-007396?style=for-the-badge&logo=openjdk&logoColor=white">
  <img src="https://img.shields.io/badge/Spring_Boot_3-6DB33F?style=for-the-badge&logo=springboot&logoColor=white">
  <img src="https://img.shields.io/badge/Spring_Data_JPA-59666C?style=for-the-badge&logo=hibernate&logoColor=white">
  <img src="https://img.shields.io/badge/QueryDSL_5-0080FF?style=for-the-badge&logoColor=white">
  <img src="https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white">
  <img src="https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white">
</div>

<div align="left" style="margin-top: 6px;">
  <img src="https://img.shields.io/badge/MySQL_8.4-4479A1?style=for-the-badge&logo=mysql&logoColor=white">
  <img src="https://img.shields.io/badge/Redis_7.4-DC382D?style=for-the-badge&logo=redis&logoColor=white">
  <img src="https://img.shields.io/badge/AWS_(EC2_/_RDS)-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white">
</div>

#### Tools & VCS
<div align="left" style="margin-top: 6px;">
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white">
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white">
  <img src="https://img.shields.io/badge/Spring_REST_Docs-6DB33F?style=for-the-badge&logo=spring&logoColor=white">
  <img src="https://img.shields.io/badge/IntelliJ_IDEA-000000?style=for-the-badge&logo=intellij-idea&logoColor=white">
</div>

---

### 🚀 Key Projects

#### 1. [견생보감 - PortOne 결제 연동 이커머스](https://github.com/Team6-Cloud-Architecture-Payment-System/payment-system)
> **기간**: 2025.03 (팀 6명) | **역할**: 인증·회원 도메인 설계, 동시성 제어, 멤버십/포인트 정합성  
> **Tech**: `Java 17`, `Spring Boot`, `Spring Security`, `JWT`, `MySQL`, `AWS`, `PortOne SDK`

- **비관적 락(Pessimistic Lock) 기반 동시성 제어 및 멱등성 보장**
  - 다수 결제 시 read-modify-write 락 부재로 인한 포인트 중복 차감 방지를 위해 `PESSIMISTIC_WRITE` 락 적용
  - 주문 ID 기반 멱등성 체크 도입으로 **동시 포인트 차감 실패율 12% → 0% 안정화**
- **동적 멤버십 등급 정책 DB화**
  - 하드코딩된 등급 기준 금액 및 적립률을 DB 정책 기반 동적 쿼리로 전환하여 **정책 변경 시 코드 수정 0건 달성**
- **단일 JWT 인증 구조 단순화**
  - 데모 인프라 특성에 맞추어 불필요한 토큰 저장소 오버헤드를 줄이고, **인증 엔드포인트 및 DTO 50% 축소**

---

#### 2. [겟츄 (Getchu) - 위치 인증 기반 지역 중고거래 플랫폼](https://github.com/Team-5th-Chat-prj/Team-5th)
> **기간**: 2025.04 (팀 4명) | **역할**: 백엔드 아키텍처 설계, 상품 CRUD, 쿼리 최적화, 캐싱 전략 수립  
> **Tech**: `Java 17`, `Spring Boot 3.2`, `Spring Data JPA`, `QueryDSL 5`, `MySQL 8.4`, `Redis 7.4`, `Docker`

- **N+1 쿼리 해결 및 응답 속도 85% 대폭 개선**
  - 상품 목록 조회 시 연관 이미지 LAZY 로딩으로 인한 N+1 문제를 QueryDSL `fetchJoin` 벌크 조회로 해결
  - **상품 20건 기준 쿼리 수 21건 → 1건 (95% 감소), 응답 시간 320ms → 45ms (85% 단축)**
- **Redis ZSET 기반 실시간 인기 검색어 집계 (DB 부하 제로화)**
  - DB COUNT/GROUP BY 집계 부하를 Redis Sorted Set(`ZINCRBY`, `ZREVRANGE`)으로 전환
  - **상위 10개 키워드 조회 시간 80ms → 5ms (93% 개선), 검색 시 DB 집계 쿼리 0건 달성**
- **QueryDSL 동적 조건 검색 캡슐화**
  - 상태·카테고리·키워드 등 다중 필터를 `BooleanBuilder` 단일 API로 통합하여 **동적 메서드 8개 → 1개로 집약**

---

#### 3. [ClueRoom - AI 기반 추리 게임 서비스](https://github.com/Final-Project-sixteam-company/project-fe)
> **기간**: 2025.05 ~ 2025.06 (팀 4명) | **역할**: API 아키텍처 조율 및 백엔드 통신 최적화, 예외 복구 구조 설계  
> **Tech**: `REST API`, `Firebase Messaging`, `Auth & Session Handling`

- **JWT 인증 예외(401) 및 세션 데드엔드(409) 2단계 복구 메커니즘 구축**
  - 토큰 유효성 사전 정제 및 실시간 세션 선조회 Fallback 경로 연계로 **세션 데드엔드 발생률 100% → 0% 달성**
- **API 스펙 정합성 최적화 & Single Source of Truth 통합**
  - 백엔드 시나리오 가이드라인 데이터 동적 주입 구조로 변경하여 **데이터 하드코딩 0건 및 유지보수성 확보**

---

#### 4. [BoardProject - 확장성 높은 게시판 시스템](https://github.com/fryzke/BoardProject)
> **개인 프로젝트** | `Java`, `Spring Boot`, `MySQL`
- 탄탄한 객체지향 설계와 모듈화를 지향하는 게시판 CRUD 및 사용자 인증 기반 프로젝트

---

### 📊 GitHub Stats

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=fryzke&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=true" height="150" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=fryzke&layout=compact&theme=tokyonight&hide_border=true" height="150" />
</div>

<div align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=fryzke&theme=tokyonight&hide_border=true" alt="GitHub Streak" />
</div>

---

### 📬 Contact
<div align="left">
 <a href="mailto:fryekdy03@naver.com">
    <img src="https://img.shields.io/badge/Naver_Mail-03C75A?style=flat-square&logo=naver&logoColor=white" />
  </a>
  <a href="https://velog.io/@fryekdy03" target="_blank">
    <img src="https://img.shields.io/badge/Velog-20C997?style=flat-square&logo=velog&logoColor=white" />
  </a>
</div>
