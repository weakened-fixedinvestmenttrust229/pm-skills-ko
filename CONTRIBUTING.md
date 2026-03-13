# 기여 안내

PM Skills 한국어판은 원본 저장소 [phuryn/pm-skills](https://github.com/phuryn/pm-skills)를 번역한 프로젝트입니다. 번역 개선, 오탈자 수정, 새 스킬 번역 추가 등의 기여를 환영합니다.

## 기여 방법

- **번역 오류 및 소규모 수정** — PR을 직접 오픈하세요.
- **신규 스킬 번역, 커맨드, 대규모 변경** — 먼저 이슈를 열어 접근 방식을 논의해주세요.

## 가이드라인

- PR은 집중적으로 — PR당 하나의 변경사항.
- 기존 패턴 준수: 스킬은 명사(도메인 지식), 커맨드는 동사(워크플로우).
- 모든 스킬에는 `name`과 `description` frontmatter 필요. 모든 커맨드에는 `description`과 `argument-hint` 필요.
- 스킬 `name`은 반드시 디렉토리명과 일치해야 함 (영어 유지).
- 커맨드에서 플러그인 간 참조 금지. 후속 작업은 자연어로만 제안.
- 제출 전 검증기 실행: `python3 validate_plugins.py`

## 번역 규칙

- `name` 필드: 영어 유지
- `description` 필드: 한국어 번역
- 본문 텍스트: 한국어 번역
- URL, 코드블록, 프레임워크 고유명사(PRD, OKR, JTBD, RICE 등): 영어 유지

## 라이선스

기여 시 [MIT License](LICENSE)에 따라 라이선스가 부여됨에 동의합니다.
