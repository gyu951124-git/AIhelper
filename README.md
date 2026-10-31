# AIhelper

GitHub Spec Kit으로 앱의 요구사항, 설계, 작업 목록을 정리하고 구현하는 프로젝트입니다.

## 설정된 환경

- Specify CLI: `1.2.5` (공식 `github/spec-kit`의 `v1.2.5` 태그)
- 패키지 관리: `uv 0.13.6`
- CLI 실행 환경: Python `3.12.11` (uv가 관리)
- AI 연동: Codex (`.agents/skills/`)
- 스크립트: Windows PowerShell
- Git 확장: 기능별 브랜치 및 순차 번호 (`001-기능명`)

## 시작하기

이 폴더에서 Codex 대화를 시작하고 아래 스킬을 순서대로 사용합니다.
스킬은 **Codex 채팅에 입력**합니다.

1. `$speckit-constitution` — 프로젝트 개발 원칙 정하기
2. `$speckit-specify 만들고 싶은 앱과 핵심 기능 설명` — 요구사항 작성
3. `$speckit-clarify` — 불명확한 요구사항 정리 (선택)
4. `$speckit-plan 사용할 기술과 제약사항 설명` — 기술 설계
5. `$speckit-tasks` — 구현 작업 목록 생성
6. `$speckit-analyze` — 요구사항·설계·작업의 일관성 확인 (선택)
7. `$speckit-implement` — 작업 목록에 따라 구현

새로 설치한 스킬이 목록에 나타나지 않으면 이 폴더에서 Codex의 새 대화를 시작합니다.
앱의 요구사항과 기술 스택은 위 절차에서 결정합니다.

## 파일 위치

- `.specify/memory/constitution.md`: 개발 원칙 템플릿
- `.specify/templates/`: 요구사항·설계·작업 문서 템플릿
- `.specify/scripts/powershell/`: 워크플로 스크립트
- `.specify/extensions/git/`: Git 워크플로 설정과 스크립트
- `.agents/skills/`: Codex용 Spec Kit 스킬
- `specs/`: 기능 명세를 작성하면 생성되는 문서 폴더

## 설치 확인 및 재설치

새 PowerShell 터미널에서 실행합니다.

```powershell
specify version
specify check
```

CLI를 같은 버전으로 설치하려면:

```powershell
uv tool install specify-cli --python 3.12 --from git+https://github.com/github/spec-kit.git@v1.2.5
```

기존 터미널에서 `specify` 명령을 찾지 못하면 터미널을 다시 열거나 아래를 실행합니다.

```powershell
$env:Path = "$env:USERPROFILE\.local\bin;$env:Path"
```

공식 안내: [설치](https://github.github.com/spec-kit/installation.html), [Codex 연동](https://github.github.com/spec-kit/integrations/codex.html)
