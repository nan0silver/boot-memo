# 🔍 Search Point Service

GitHub 소셜 로그인을 통해 검색 및 북마크 기능을 사용할 수 있으며, 포인트를 소모하거나 광고를 시청하여 포인트를 충전하는 Spring Boot 기반의 웹 서비스입니다.

## 💡 주요 기능

- 🔐 GitHub 소셜 로그인 (OAuth2)
- 🔐 Spring Security 기반 유저 인증 및 권한 관리
- 🔎 외부 검색 OPEN API 연동
- 💰 포인트 시스템
    - 검색 시 포인트 차감
    - 북마크 시 포인트 차감
    - 광고 시청 시 포인트 충전
- 🔒 BCrypt 비밀번호 암호화
- 🌐 CSRF 보호 및 예외 처리
- 📄 사용자 친화적 예외 메시지 및 에러 페이지
- 📦 MyBatis + PostgreSQL 연동

## 🛠️ 기술 스택

- **Backend**: Java 17, Spring Boot 3, Spring Security 6, MyBatis
- **Database**: PostgreSQL
- **Authentication**: OAuth2 (GitHub)
- **Template Engine**: Thymeleaf
- **Build Tool**: Gradle
- **CI/CD**: Docker, GitHub Actions (예정)

## 📁 프로젝트 구조 (간략)
```
src
└── main
├── java
│   └── com.example.searchpoint
│       ├── auth        # 로그인/로그아웃, OAuth 처리
│       ├── user        # 유저 서비스 및 유저 도메인
│       ├── point       # 포인트 차감/충전 로직
│       ├── bookmark    # 북마크 기능
│       └── search      # 검색 API 연동
└── resources
├── templates       # Thymeleaf 템플릿
├── static          # 정적 파일 (css, js 등)
└── application.yml
```