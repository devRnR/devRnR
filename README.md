# 권용수 · logcat

**틀리면 되돌리기 어려운 경로**를 주로 다뤄 왔습니다 — 150억이 오가는 자금 집행, 두 번 가면 안 되는 알림, 재고가 음수가 되면 안 되는 차감.

여기서는 정합성과 동시성이 '있으면 좋은 것'이 아니라 전제 조건이라, 문제가 생기면 증상에서 멈추지 않고 프레임워크 내부까지 내려가 원인을 확인합니다.

도입할 근거를 말할 수 있으려면 **도입하지 않을 근거**도 같이 말할 수 있어야 한다고 봅니다. 그래서 만든 것마다 "이 설계를 안 쓸 조건"을 같이 적어 둡니다.

---

### 최근 작업

| | |
|---|---|
| **[타임딜 재고 차감](https://github.com/logcat-io/ecommerce-sample-with-springboot-kotlin-jooq)** | 확정 실패할 요청을 DB 도달 전에 버려 커넥션 풀을 지킨다. 필터만 무력화한 대조군과 풀 크기 스윕으로 효과·경계·안 쓸 조건까지 측정 · `Kotlin` `Spring Boot 4` `jOOQ` `PostgreSQL` `Redis` |
| **[Reliable Webhook Dispatcher](https://github.com/logcat-io/reliable-webhook-dispatcher-golang)** | 회사에서 운영 배포까지 가지 못한 Outbox 전송 신뢰성 구조를 바닥부터 다시 구현. 유실·중복 0건 실측, `go test -race` 통과 · `Go` `PostgreSQL` `Prometheus` |
| **[tinyredis](https://github.com/logcat-io/go-tiny-redis)** | 표준 라이브러리만으로 만든 Redis 미니 클론. RESP 파서 · TTL · 스냅샷 · graceful shutdown, redis-cli/redis-benchmark 호환 · `Go` |
| **[trove](https://github.com/logcat-io/trove)** · **[shove](https://github.com/logcat-io/shove)** | 직접 쓰려고 만든 macOS 메뉴바 유틸 · `Swift` |

### 다루는 것

`Java` `Kotlin` `Spring Boot` `Spring Batch` `JPA` `jOOQ` · `Go`
`PostgreSQL` `MySQL` `Redis` · `AWS` `Docker`

### 기록

배운 것과 틀린 것을 남깁니다. MVCC·InnoDB 버퍼풀·프레임워크 내부까지 파고든 학습 노트 **81편**.

[![Blog](https://img.shields.io/badge/blog-logcat--io.github.io-181717?style=flat-square&logo=github&logoColor=white)](https://logcat-io.github.io/)
[![Email](https://img.shields.io/badge/yskwon0619@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:yskwon0619@gmail.com)
