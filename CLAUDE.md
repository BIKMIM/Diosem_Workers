# Diosem Workers — 기술팀 작업 배정 현황

## 프로젝트 개요
- 단일 파일 HTML 앱 (`index.html`) — 프레임워크 없음
- GitHub Pages로 배포: https://bikmim.github.io/Diosem_Workers/
- GitHub 저장소: https://github.com/BIKMIM/Diosem_Workers

## 관련 프로젝트
- **영업팀 버전**: `Diosem_work_manager_sales` 폴더 — React JS, 더 복잡한 구조

## 직원 명단 (기술팀 21명, 직급 순서)
이상엽, 서한주, 강범일, 최광섭, 조광호, 최현철, 김진탁, 신재웅, 권용덕, 김태영,
노진성, 장다빈, 조용준, 신지호, 고상원, 박정민, 박경식, 임영곤, 윤호진, 박준경, 김은우

- 명단 변경 시 `index.html` 내 `allWorkers` 배열과 버튼 텍스트(`기술팀 총 21명`) 동시 수정

## 버전 관리
- 버전 표기: `index.html` 하단 `.version` div
- 버전 형식: `Version: X.XX 변경내용 · YYYY-MM-DD`
- 현재 버전: 1.80
- Git으로 관리 — 폴더별 버전 분리 안 함

## 주요 기능
- 주간 작업 내용 붙여넣기 → 요일별 미배정 인원 자동 추출
- 연차(8h) / 반차(4h) / 반반차(2h) / 교육(차감없음) 처리
- 법정 공휴일 자동 인식 (2025~2027년 데이터 내장)
- 주간 누적 잔업 시간 계산 및 상세 내역 팝업

## 작업 규칙
- 날짜 형식: `<6월 9일 월요일>` 형태로 파싱
- 작업 라인: `■ ◆ □ ★` 으로 시작
- 공휴일 키워드: `FIXED_HOLIDAY_NAMES`, `VARIABLE_HOLIDAYS` 상수에서 관리
- 반반차 키워드: `HALF_HALF_LEAVE_KEYWORD` 상수 (`'반반차'`)
