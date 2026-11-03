# E1-1. 개발 워크스테이션 구축

> 터미널·Docker·Git을 직접 세팅하고, 실행 결과(로그·접속·데이터 유지)로 동작을 검증한 기록

<!-- TODO 표시는 실습하면서 실제 출력/스크린샷으로 교체 -->

## 목차
1. [프로젝트 개요](#1-프로젝트-개요)
2. [실행 환경](#2-실행-환경)
3. [수행 체크리스트](#3-수행-체크리스트)
4. [저장소 구조](#4-저장소-구조)
5. [수행 로그](#5-수행-로그)
6. [보너스 과제](#6-보너스-과제)
7. [개념 정리](#7-개념-정리)
8. [트러블슈팅](#8-트러블슈팅)
9. [재현 방법](#9-재현-방법)
10. [보안 및 개인정보 처리](#10-보안-및-개인정보-처리)

---

## 1. 프로젝트 개요
- 목표: TODO (미션 목표를 내 말로 2~3줄)
- 핵심 흐름: 터미널/권한 정리 → Docker 설치·점검 → 컨테이너 운영 → Dockerfile 커스텀 이미지 → 포트 매핑 → 바인드 마운트/볼륨 → Git/GitHub 연동

## 2. 실행 환경
| 항목 | 값 |
|---|---|
| Host OS | Windows 11 Home |
| Linux 환경 | WSL2 / Ubuntu TODO(버전) |
| Shell / Terminal | bash / Windows Terminal TODO |
| Docker | TODO (`docker --version`) |
| Docker Compose | TODO (`docker compose version`) |
| Git | TODO (`git --version`) |
| Editor | VSCode + WSL 확장 |

## 3. 수행 체크리스트
### 필수
- [ ] 터미널 기본 조작 (이동/생성/복사/이동·이름변경/삭제/내용 확인/빈 파일)
- [ ] 권한 변경 실습 (파일 1, 디렉토리 1)
- [ ] Docker 설치 및 점검 (`--version`, `info`)
- [ ] Docker 기본 운영 (images, ps, logs, stats)
- [ ] hello-world 실행
- [ ] ubuntu 컨테이너 진입 및 attach/exec 차이 관찰
- [ ] Dockerfile 커스텀 이미지 빌드·실행 (nginx 기반)
- [ ] 포트 매핑 접속 (2개 포트)
- [ ] 바인드 마운트 변경 반영
- [ ] Docker 볼륨 영속성
- [ ] Git 설정 + VSCode GitHub 연동

### 보너스
- [ ] Docker Compose 단일 서비스
- [ ] Docker Compose 멀티 컨테이너 + 네트워크 통신
- [ ] Compose 운영 명령 (up/down/ps/logs)
- [ ] 환경 변수로 포트/모드 변경
- [ ] GitHub SSH 키 설정

## 4. 저장소 구조
```text
E1-1/
├── README.md
├── app/
│   ├── Dockerfile        # 커스텀 nginx 이미지
│   └── site/             # 정적 웹 콘텐츠
├── compose/              # 보너스: docker-compose.yml
├── docs/
│   └── screenshots/      # 브라우저/VSCode 캡처
└── logs/                 # 터미널 원본 로그 (선택)
```

---

## 5. 수행 로그

### 5-1. 터미널 기본 조작
> 확인 내용: 현재 위치, 숨김 파일 포함 목록, 이동, 생성, 복사, 이동/이름변경, 삭제, 내용 확인, 빈 파일 생성
```bash
# TODO
```

### 5-2. 권한 실습
> 확인 내용: 파일 1개·디렉토리 1개의 권한 변경 전/후 비교
```bash
# TODO
```
| 대상 | 변경 전 | 변경 후 | 의미 |
|---|---|---|---|
| 파일 | TODO | TODO | TODO |
| 디렉토리 | TODO | TODO | TODO |

### 5-3. Docker 설치 및 점검
> 확인 내용: Docker CLI 버전, 데몬(서버) 동작 여부
```bash
# TODO: docker --version / docker info (발췌)
```

### 5-4. Docker 기본 운영 명령
```bash
# TODO: docker pull / images / run / stop / ps / ps -a / logs / stats --no-stream
```

### 5-5. 컨테이너 실행 실습
#### hello-world
```bash
# TODO
```
#### ubuntu 컨테이너 진입
```bash
# TODO
```
#### attach vs exec 관찰
| 구분 | 동작 | 빠져나왔을 때 컨테이너 상태 |
|---|---|---|
| `docker attach` | TODO | TODO |
| `docker exec -it` | TODO | TODO |

### 5-6. 커스텀 이미지 (방식 A: nginx 베이스)
- 선택한 베이스: TODO (이미지명:태그, 선택 이유)
- 커스텀 포인트

| 커스텀 포인트 | 목적 |
|---|---|
| TODO | TODO |

```bash
# TODO: docker build / docker run 결과
```

### 5-7. 포트 매핑 및 접속 확인
```bash
# TODO: 두 개의 호스트 포트로 실행 + curl
```
![포트 매핑 접속 1](docs/screenshots/TODO.png)
![포트 매핑 접속 2](docs/screenshots/TODO.png)

### 5-8. 바인드 마운트 변경 반영
```bash
# TODO: 실행 명령 / 변경 전 응답 / 호스트 파일 수정 / 변경 후 응답
```

### 5-9. Docker 볼륨 영속성
```bash
# TODO: volume create / 연결 / 데이터 기록 / 컨테이너 삭제 / 새 컨테이너에서 확인
```

### 5-10. Git 설정 및 GitHub 연동
```bash
# TODO: git config --list (민감 항목 마스킹)
```
![VSCode GitHub 연동](docs/screenshots/TODO.png)

---

## 6. 보너스 과제
### 6-1. Compose 단일 서비스
### 6-2. Compose 멀티 컨테이너 + 네트워크 통신
### 6-3. Compose 운영 명령
### 6-4. 환경 변수 활용
### 6-5. GitHub SSH 키

---

## 7. 개념 정리
- **절대 경로 vs 상대 경로**: TODO (예시 포함)
- **파일 권한 r/w/x, 755/644 해석 규칙**: TODO
- **이미지 vs 컨테이너**: TODO
- **포트 매핑이 필요한 이유**: TODO
- **바인드 마운트 vs 볼륨**: TODO
- **Git vs GitHub**: TODO

## 8. 트러블슈팅
### 8-1. TODO 제목
- 문제:
- 원인 가설:
- 확인:
- 해결/대안:

### 8-2. TODO 제목
- 문제:
- 원인 가설:
- 확인:
- 해결/대안:

## 9. 재현 방법
```bash
# TODO: clone → build → run → 접속 확인까지 최소 명령
```
- 주의사항: TODO (WSL 경로, 포트 충돌 시 대체 포트 등)

## 10. 보안 및 개인정보 처리
- 로그/스크린샷의 토큰·비밀번호·개인키·인증코드는 마스킹
- `git config --list`, `docker info`의 계정 관련 항목 확인 후 마스킹
- `.env`, 개인키 파일은 `.gitignore`로 커밋 제외
