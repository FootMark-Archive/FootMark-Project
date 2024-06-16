# FootMark-Project
발자국을 따라 떠올려 보세요

# Swagger
https://handmark.shop/swagger-ui/index.html

# Server

## 기술 버전

- **Java**: 17
- **Spring Boot**: 3.2.3
- **Spring Data JPA**: 최신 Spring Boot 호환 버전
- **Spring Web**: 최신 Spring Boot 호환 버전
- **Spring Validation**: 최신 Spring Boot 호환 버전
- **Lombok**: 최신 버전
- **H2 Database**: 최신 버전
- **MariaDB JDBC**: 최신 버전
- **Spring Security**: 최신 Spring Boot 호환 버전
- **JSON Web Token (JWT)**:
  - `io.jsonwebtoken:jjwt-api`: 0.11.5
  - `io.jsonwebtoken:jjwt-impl`: 0.11.5
  - `io.jsonwebtoken:jjwt-jackson`: 0.11.5
- **OAuth2 Client**: 최신 Spring Boot 호환 버전
- **Swagger (Springdoc OpenAPI)**:
  - `org.springdoc:springdoc-openapi-starter-common`: 2.0.2
  - `org.springdoc:springdoc-openapi-starter-webmvc-ui`: 2.0.2
- **QueryDSL**:
  - `com.querydsl:querydsl-jpa`: 5.0.0:jakarta

## 프로젝트 빌드 및 실행 절차

### 전제 조건

- **Java Development Kit (JDK)**: 버전 17 이상 설치
- **Gradle**: 프로젝트는 Gradle을 사용하므로 Gradle이 설치되어 있어야 함
- **IDE**: IntelliJ IDEA 또는 Eclipse 같은 Java IDE 설치 권장
- **Database**: MariaDB 설치 및 설정

### 1. 프로젝트 클론

GitHub 또는 다른 소스 코드 관리 시스템에서 프로젝트 클론.

```bash
git clone <project-url>
cd <project-directory>
```

### 2. 데이터베이스 설정
```properties
spring.datasource.url=jdbc:mariadb://localhost:3306/your_database
spring.datasource.username=your_username
spring.datasource.password=your_password
```

### 3. QueryDSL 설정
```bash
./gradlew compileQuerydsl
```

### 4. 프로젝트 빌드
```bash
./gradlew clean build
```

### 5. 프로젝트 실행
```bash
./gradlew bootRun
```

### 6. API 테스팅 (Postman 및 Swagger 사용)
- **Postman**: Postman에서 새로운 컬렉션을 생성하고 API 엔드포인트를 테스트합니다.
- **Swagger**: 애플리케이션이 실행 중일 때, 브라우저에서 http://localhost:8080/swagger-ui.html에 접속하여 Swagger UI를 사용해 API를 테스트합니다.
