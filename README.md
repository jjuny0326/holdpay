# HoldPay

### 중고거래 안전결제(에스크로) 서비스입니다.

* 돈을 먼저 보냈는데 물건이 오지 않는 중고거래 사기를 막기 위해 만들었습니다.
* 구매자가 결제한 금액을 서비스가 보관하고 있다가, 구매자가 물건을 받고 구매를 확정하면 판매자에게 정산합니다.

## 기술 스택

- Java 25, Spring Boot 4, Spring Data JPA
- PostgreSQL 17
- Docker Compose

## 로컬 실행

1. DB 실행

```bash
docker compose up -d
```

2. 앱 실행

```bash
./gradlew bootRun        # macOS, Linux
.\gradlew.bat bootRun    # Windows
```

3. 확인

http://localhost:8080/actuator/health 에서 `"status": "UP"`이 나오면 정상입니다.

DB를 끌 때는 `docker compose down`을 실행합니다.

## 진행 상황

- [x] 프로젝트 생성, PostgreSQL 연결
- [ ] 회원가입·로그인 (JWT)
- [ ] 에스크로 거래 흐름
- [ ] 결제 연동
- [ ] AWS 배포