# StayLog (Frontend)
> **사용자 친화적인 UI/UX를 갖춘 숙소 예약 & 커뮤니티 서비스**

## Project Overview
**StayLog**는 실시간 알림과 커뮤니티 기능을 결합하여 사용자에게 끊김 없는 예약 경험을 제공하는 웹 애플리케이션입니다.
백엔드 API와의 효율적인 통신을 위해 **TypeScript** 기반의 엄격한 타입 지정과 SSE(Server-Sent Events)를 활용한 실시간 데이터 처리에 중점을 두었습니다.

* 프로젝트 기간: 2025.10.13 ~ 2025.11.12 (4주)
* 팀 구성: 총 9명 (Backend & Frontend 풀스택 협업)
* **Backend Repository:** https://github.com/infreeJ/staylog-backend
* **Service URL:** https://staylog.store/

---

## 스크린샷

| 메인 페이지 | 실시간 알림 |
| :---: | :---: |
| <img width="600" alt="staylog_main" src="https://github.com/user-attachments/assets/4689fcbf-30c7-4770-abff-93d565facbd0" /> | <img width="200" alt="쿠폰모달" src="https://github.com/user-attachments/assets/35a6d1c1-491b-4ac5-af2a-d1d0b0dda92a" /> |

| 쿠폰함 | 회원가입 |
| :---: | :---: |
| <img width="400" alt="사용가능쿠폰" src="https://github.com/user-attachments/assets/3b0c9d30-3f1d-4475-a78c-b435a1418141" /> | <img width="300" alt="회원가입 확대" src="https://github.com/user-attachments/assets/944ab88d-460f-4f52-b8c9-7c154bb6fa6a" /> |

---


## 내가 기여한 부분

### 1. 실시간 알림 처리
* **구현 내용:** 백엔드의 SSE 엔드포인트와 `EventSource`를 연결하여, 새로고침 없이 서버로부터 실시간으로 알림을 수신합니다.
* **UX 개선:** 알림 수신 시 즉각적인 알림 카드 PUSH와 알림 아이콘의 배지 카운트를 갱신하여 사용자가 정보를 놓치지 않도록 구현했습니다.

### 2. 할인 쿠폰 시스템
* **구현 내용:** 결제 시 모달 인터페이스를 통해 보유 쿠폰 목록을 호출하며, **사용 가능과 사용 불가 탭을 분리**하여 데이터 시인성을 높였습니다.
* **UX 개선:** 쿠폰 적용 버튼 클릭 시, 전체 결제 금액에서 할인액이 차감된 최종 금액을 동적으로 재계산 하여 즉각적인 시각적 피드백을 제공합니다.

### 3. 안정적인 데이터 통신
* **타입 안정성:** 백엔드와 협의된 API 명세서(Swagger 등)를 기반으로 `Interface`를 명확히 정의하여, 런타임 데이터 오류를 방지하고 유지보수성을 높였습니다.

### 4. 유효성 검증
* **3단계 검증:** 회원가입 및 예약 입력 폼에서 정규표현식을 활용한 즉각적인 유효성 검사를 수행합니다.
* **서버 부하 감소:** 불필요한 요청이 서버로 전송되는 것을 클라이언트 단에서 사전에 차단하여 서버 리소스를 절약했습니다.

---
