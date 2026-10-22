# 안녕하세요, 프론트엔드 개발자 윤지원입니다 👋

서비스의 **완성도**와 **구조적 유지보수성**을 함께 고민합니다.
UI 구현을 넘어, 오래 쓸 수 있는 구조와 사용자가 이해하기 쉬운 UX를 만드는 데 관심이 많습니다.

- 🧩 기능별 컴포넌트와 공통 UI를 분리하고, Service + TanStack Query 기반 Custom Hook으로 비동기 로직을 모듈화합니다.
- 🔄 서버 상태값을 그대로 노출하지 않고, 사용자 관점의 UI 상태로 가공합니다.
- ⚡ 캐싱 전략으로 불필요한 요청을 줄이는 등 기능 구현을 넘어 효율까지 고려합니다.
- 🔍 에러를 만나면 코드뿐 아니라 원인이 되는 상태와 환경까지 끝까지 추적합니다.
- ✍️ 블로그 기록과 스터디 운영으로 배운 것을 나누며 꾸준히 성장하고 있습니다.

## 🛠 Tech Stack

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)

![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![TanStack Query](https://img.shields.io/badge/TanStack_Query-FF4154?style=flat-square&logo=reactquery&logoColor=white)
![Zustand](https://img.shields.io/badge/Zustand-433E38?style=flat-square)
![Axios](https://img.shields.io/badge/Axios-5A29E4?style=flat-square&logo=axios&logoColor=white)

![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=flat-square&logo=figma&logoColor=white)

![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white)
![Gemini API](https://img.shields.io/badge/Gemini_API-8E75B2?style=flat-square&logo=googlegemini&logoColor=white)

![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)
![Jira](https://img.shields.io/badge/Jira-0052CC?style=flat-square&logo=jira&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)

## 🚀 Projects

### [DengMate](https://github.com/jiwonll/daeng-mate) · 개인 프로젝트 (2026.07 ~ 진행 중)
위치 기반으로 산책 메이트를 모집하고, 실시간 산책 기록까지 관리할 수 있는 반려견 산책 매칭 서비스

- **역할**: 기획 및 프론트엔드 개발, Supabase 기반 인증·데이터베이스 연동
- **담당**: 메인, 산책 기록, 메이트 매칭, 설정(마이) 페이지
- **Stack**: Next.js 16 (App Router), React 19, TypeScript (strict), Tailwind CSS v4, TanStack Query, Zustand, Supabase
- **Troubleshooting**
  - Next.js App Router + Supabase 카카오 로그인 **무한 리다이렉트** 해결 (미들웨어 요청·응답 쿠키 동기화, 인증 콜백 경로 예외 처리, 프록시 환경별 리다이렉트 분기)
  - 비밀번호 변경 시 특정 계정에서 반복되던 **Auth 에러 원인 추적** (이메일 인증 상태·로그인 방식에 따른 예외 처리와 안내 메시지 개선)
- 🔗 [배포 URL](https://daeng-mate.vercel.app/)

### [Mappia](https://github.com/hanpla/Mappia) · Codeit 부트캠프 팀 프로젝트 (2026.05 ~ 2026.06, 프론트엔드 5인)
체험 상품 등록, 예약 신청, 승인 프로세스를 통합 관리하는 체험 예약 플랫폼

- **담당**: 예약 내역 페이지, 공통 Color/Button 컴포넌트, 커스텀 캘린더, 후기 작성/조회 및 Gemini AI 후기 요약
- **Stack**: Next.js 16 (App Router), React 19, TanStack Query, Zustand, TypeScript (strict), Tailwind CSS v4
- **Troubleshooting**
  - 백엔드 수정 없이 **AI 요약 재호출 시점 설계**: 리뷰 개수 변화를 기준으로 커스텀 훅에서 요약 결과를 localStorage에 캐싱하고, 변화가 있을 때만 Gemini API 재호출
  - 체험 종료 후 갱신되지 않는 **예약 상태값 보정**: 서버 상태를 사용자 관점의 UI 상태로 가공
  - 일정 식별자 부재로 인한 **후기 데이터 매칭 오류 해결** 및 순차 유효성 검증 도입
- 🔗 [배포 URL](https://mappia23.vercel.app/)

### Taskify · Codeit 부트캠프 팀 프로젝트 (2026.04 ~ 2026.05)
개인 스케줄 관리를 넘어 타인과 일정을 공유하고 협업하는 커뮤니티형 스케줄러

- **담당**: 레이아웃(헤더·푸터), 할 일(Todo) CRUD, 이미지 업로드 컴포넌트
- **Troubleshooting**
  - 할 일 수정 모달의 이미지 업로드 상태를 **파일 객체와 삭제 플래그로 분리**해 유지/삭제/신규 업로드 상태를 명확히 정의
  - `<input type="file">` 재선택 예외를 **동적 key 바인딩 리마운트**로 해결

### 💬 OpenMind · Codeit 부트캠프 팀 프로젝트 (2026.03)
익명으로 질문을 주고받고, 답변을 피드로 공유하는 소셜 네트워크 서비스

- **담당**: 전체 피드 조회(List) 페이지
- **Troubleshooting**
  - `useState` 기반 호버 애니메이션을 **CSS `:hover` 전환으로 리팩토링**해 hover 10회 기준 커밋 20회 → 0회로 감소 (React Profiler 측정)
  - API 고속 응답 시 로딩 스피너 깜빡임을 **Delayed Display** 로직으로 개선

## 📫 Contact

- 📝 Blog: [velog.io/@jiwon-frontend](https://velog.io/@jiwon-frontend/posts)
- 📧 Email: yoonjw4966@naver.com
