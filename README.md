# p-13959-mission-3
## ✅ SBB 서비스 배포 완료

### 🔗 배포 주소
- [https://상현sbb.world](https://xn--sbb-2y4np46f.world/)
- 

---

### ✅ 구현한 항목 (점프 투 스프링부트 4장 기준)

- [x] 4-01 이제 서버가 필요하다!
- [x] 4-02 AWS 라이트세일 알아보기
- [x] 4-03 서버 접속 설정하기
- [x] 4-04 서버 접속 프로그램 설치하기
- [x] 4-05 SBB 배포하기
- [x] 4-06 서버 스크립트 생성하기
- [x] 4-07 서버 환경으로 분리하기 (`application-prod.yml`)
- [x] 4-08 80번 포트로 웹 서비스 운영하기 (Nginx 리버스 프록시 설정)
- [x] 4-09 로그 관리하기 (`nohup`, `tail -f logs/sbb.log`)
- [x] 4-10 도메인 사용하기 (`sbb.world`, Route53 또는 Freenom 사용)
- [x] 4-11 HTTPS로 전환하기 (Let's Encrypt + Certbot 인증서 설치)
- [x] 4-12 PostgreSQL로 전환하기 (`application-prod.yml` 설정 완료)

---

### 🛠 사용한 서버 환경

- Ubuntu 22.04 (AWS Lightsail)
- 고정 IP: 3.39.39.69
- Nginx + Spring Boot 실행 (포트 8080 → Nginx 리버스 프록시 통해 80/443 노출)
- PostgreSQL 연동 (JDBC URL, 사용자/비밀번호 환경변수로 분리)

---

### 💡 추가 설정 및 보안 조치

- `ufw`로 22, 80, 443 포트만 허용
- `nohup`으로 백그라운드 실행
- `logrotate` 설정으로 로그 순환 가능

---

### 📌 배포 스크립트 예시

```bash
# build + deploy
./deploy.sh
