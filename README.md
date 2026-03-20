# 오스템임플란트 AI 업무개선 프로젝트 — 3조

> 재경총괄본부 · AI 활용역량 개선 TF

---

## 이 저장소는 무엇인가요?

3조가 맡은 과제를 **AI로 자동화**하는 코드와 데모 앱을 모아놓은 저장소입니다.

| 구분 | 경로 | 설명 |
|------|------|------|
| **프로젝트 규칙** | `RULES.md` | 초보자용 프로젝트 가이드 & 규칙 |
| **데모 앱** | `demos/` | 과제별 시연용 앱 (HTML / Streamlit / Tkinter) |
| **자동화 코드** | `examples/` | 과제별 실제 업무 자동화 Python 코드 |

---

## 12개 과제 목록

| # | 과제명 | 범주 |
|---|--------|------|
| 1 | 관리회계 실적 정리 자동화 (VBA/PowerQuery) | Excel DB화 |
| 2 | 법인별 손익변동 항목 추출 (AI 필터링) | AI 판단 |
| 3 | 이상출고 위험 관리 (모니터링 + 메일) | 관리시스템 |
| 4 | 환율·주가 자동 업데이트 | RPA 자동화 |
| 5 | 결산명세서 검증 AI-tool | AI 판단 |
| 6 | 자연어 검색을 통한 실적 분석 (RAG) | AI 판단 |
| 7 | 외부기장 업체 Data 적정성 검증 | AI 판단 |
| 8 | 내부회계관리제도 운영평가 샘플링 | RPA 자동화 |
| 9 | 해외법인 레포트 취합 합산 | Excel DB화 |
| 10 | Netra 리포트 자동 다운 및 가공 | RPA 자동화 |
| 11 | GRIR 반제 결과 리스트 자동화 | RPA 자동화 |
| 12 | 환율 보고서 AI 자동 작성 | 관리시스템 |

---

## 시작하기

```bash
# 1. 저장소 받기
git clone https://github.com/rammmaa/Osstem-AI-3.git
cd Osstem-AI-3

# 2. 가상 환경 만들기
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt

# 3. 환경변수 설정
cp .env.example .env
# .env 파일을 열어 API 키 입력
```

---

## 기술 스택

- **언어**: Python 3.11+
- **데이터 처리**: pandas, openpyxl, NumPy
- **API 연동**: requests, anthropic (Claude API)
- **DB**: SQLite
- **PDF 처리**: pdfplumber / PyPDF2

---

## 보안 원칙

1. API 키·비밀번호는 환경변수(`.env`)로만 관리
2. `.env` 파일은 `.gitignore`에 포함하여 절대 커밋하지 않음
3. 예시 데이터는 실제가 아닌 더미 데이터 사용
4. 로그에 민감 정보 출력 금지
