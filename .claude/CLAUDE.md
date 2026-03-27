# 오스템임플란트 AI 업무개선 프로젝트 — 3조

## 프로젝트 개요
재경총괄본부 AI 활용역량 개선 TF 3조의 과제별 자동화 코드 및 데모 앱 저장소

## 구조
- `demos/` — 과제별 시연용 데모 앱 (HTML / Streamlit / Tkinter)
- `examples/` — 과제별 업무 자동화 Python 코드
- `RULES.md` — 초보자용 프로젝트 가이드 & 규칙

## 코딩 컨벤션
- Python 3.11+, 타입 힌트 필수
- 한국어 주석/문서
- 보안: API 키/비밀번호는 반드시 환경변수 사용
- 더미 데이터만 커밋 (실제 업무 데이터 커밋 금지)

## 문서 현황

| 문서 | 상태 | 설명 |
|------|------|------|
| `README.md` | ✅ 완료 | 초보자 친화적으로 전면 재작성 |
| `RULES.md` | ✅ 완료 | 초보자용 프로젝트 가이드 & 규칙 |
| `CLAUDE.md` | ✅ 완료 | AI용 프로젝트 설명서 (이 파일) |
| `.gitignore` | ✅ 완료 | Git 제외 파일 목록 |
| `.env.example` | ✅ 완료 | 환경변수 양식 |

## Claude Code 설정 (.claude/)

| 파일 | 용도 |
|------|------|
| `CLAUDE.md` | AI용 프로젝트 설명서 (이 파일) |
| `RULES.md` | 초보자용 프로젝트 가이드 & 규칙 |
| `settings.json` | Claude Code 프로젝트 설정 (권한, 훅, 언어) |
| `commands/save.md` | `/save` 명령어 — CLAUDE.md 업데이트 + commit & push 통합 커맨드 |

### settings.json 주요 설정
- **언어**: 한국어 응답
- **허용 명령**: python, pip, git, streamlit, ls, 파일 읽기/검색
- **차단 명령**: `rm -rf`
- **보안 훅**: 코드 작성 시 API 키/비밀번호 하드코딩 자동 감지 (PreToolUse)

## 슬래시 커맨드

| 명령어 | 설명 |
|--------|------|
| `/save` | CLAUDE.md 자동 업데이트 → 변경사항 commit → push (올인원) |

## 진행 현황

- README.md 초보자 친화적 전면 재작성 완료
  - 폴더 설명을 비유 형태로 변경 ("이 서랍에는 뭐가 들어있나요?")
  - 12개 과제에 한 줄 설명 추가 (범주 → 실제 기능 설명)
  - 시작하기 가이드를 4단계로 분리 + 각 단계별 설명 추가
  - 기술 스택 표에 용도 설명 추가
  - 보안 규칙을 "해야 할 것 / 하면 안 되는 것" 대비 표로 정리
- .claude/ 디렉토리 설정 완료 (2026-03-27)
  - `settings.json` 생성 (한국어, 권한, 보안 훅)
  - `.gitignore`에 `settings.local.json` 추가
  - `/save` 통합 슬래시 커맨드 생성 (CLAUDE.md 업데이트 + commit + push)
