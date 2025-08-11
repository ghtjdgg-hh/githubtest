# 프로젝트명 (예: KD Insurance Admin)

![CI](https://github.com/YOUR_GH_ID/YOUR_REPO/actions/workflows/ci.yml/badge.svg)
![License](https://img.shields.io/badge/License-MIT-lightgrey)
![Stack](https://img.shields.io/badge/Java-17-red?logo=java)
![Spring](https://img.shields.io/badge/Spring-Framework-green?logo=spring)
![DB](https://img.shields.io/badge/Oracle-DB-orange?logo=oracle)

## ✨ Features
- 고객/피보험자/계약/공지 **CRUD**
- 로그인/권한 (Spring Security)
- 댓글 AJAX (REST API)

## 🧱 Tech Stack
- Backend: Java 17, Spring MVC/Security, MyBatis
- DB: Oracle
- Front: JSP, JSTL, Bootstrap, AJAX

## 🚀 Quick Start
```bash
# 1) 환경변수 또는 application-*.properties에 DB 접속 정보 설정
# 2) 빌드
mvn clean package -DskipTests
# 3) 실행 (부트가 아니면 톰캣 배포)
