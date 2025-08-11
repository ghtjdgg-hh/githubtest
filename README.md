# 🏢 KD 손해보험 관리자 시스템

![Java](https://img.shields.io/badge/Java-17-red?logo=java)
![Spring MVC](https://img.shields.io/badge/Spring-MVC-green?logo=spring)
![MyBatis](https://img.shields.io/badge/MyBatis-💾-orange)
![Oracle](https://img.shields.io/badge/Oracle-DB-informational?logo=oracle)
![Bootstrap](https://img.shields.io/badge/Bootstrap-🟣-purple?logo=bootstrap)

## 📌 프로젝트 소개
**KD 손해보험 관리자 시스템**은 보험사 내부 관리자가 사용하는 백오피스 웹 애플리케이션입니다.  
고객, 피보험자, 계약, 공지사항 관리 등 주요 보험 업무를 웹 환경에서 처리할 수 있도록 설계되었습니다.  
`Spring MVC + MyBatis + Oracle` 기반으로 구축되었으며, 로그인/권한 처리와 UI 디자인은 **Material Dashboard 3**를 적용했습니다.

---

## ✨ 주요 기능

### 1. 고객/피보험자 관리
- 신규 등록, 수정, 삭제, 상세 조회
- 고객별 계약 현황 확인

### 2. 계약 관리
- 계약 등록/수정/삭제
- 계약 시작일/종료일, 상태 관리
- 고객·피보험자 외래키 연동
- 최근 등록 계약 대시보드 출력

### 3. 공지사항 관리
- 공지 등록/수정/삭제
- 목록/상세 보기
- **댓글 기능** (AJAX 기반, 등록/조회)

### 4. 로그인/권한 관리
- **Spring Security** 기반 관리자 로그인
- BCrypt 비밀번호 암호화
- 세션 관리 및 접근 제어

### 5. UI/디자인
- **Material Dashboard 3** 적용
- 반응형 사이드바 메뉴
- 차트/통계 위젯 연동

---

## 🧱 기술 스택

| 구분       | 기술 |
|------------|------|
| Language   | Java 17, SQL |
| Framework  | Spring MVC, Spring Security |
| ORM/DB     | MyBatis, Oracle Database |
| Frontend   | JSP, JSTL, Bootstrap, Material Dashboard 3, AJAX |
| Server     | Apache Tomcat |
| Tools      | Eclipse, Git/GitHub |
| Build Tool | Maven |

---

## 📐 ERD
![ERD](docs/erd.png)

> 주요 테이블: `customer`, `insured_person`, `contract`, `notice`, `admin_user`, `reply`  
> `contract.customer_id` → `customer.customer_id` (FK)  
> `contract.insured_id` → `insured_person.insured_id` (FK)

---

## 📸 화면 예시

| 화면 | 설명 |
|------|------|
| ![login](docs/login.png) | 관리자 로그인 |
| ![dashboard](docs/dashboard.png) | 대시보드(최근 계약/공지) |
| ![customer](docs/customer.png) | 고객 관리 |
| ![contract](docs/contract.png) | 계약 등록/수정 |
| ![notice](docs/notice.png) | 공지사항 관리 |
| ![reply](docs/reply.png) | 댓글 AJAX |

---

## 🚀 설치 및 실행 방법

```bash
# 1. 저장소 클론
git clone https://github.com/YOUR_GH_ID/kd-insurance-admin.git
cd kd-insurance-admin

# 2. Oracle DB에 테이블 생성 및 샘플 데이터 삽입
# (docs/sql/schema.sql 참고)

# 3. Maven 빌드
mvn clean package -DskipTests

# 4. Tomcat에 배포 후 실행
