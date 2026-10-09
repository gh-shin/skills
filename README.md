# Skills

개인 작성 Agent Skills 모음입니다.

| 스킬 | 용도 |
| --- | --- |
| [report-polish](report-polish/SKILL.md) | 한국어 문서를 개조식 보고서로 요약·윤문 |
| [tech-report](tech-report/SKILL.md) | 기술·평가 보고서, 실험 기록, 설계 결정, 장애 분석의 작성·수정·검토 |

## 설치

Node.js 22.20.0 이상과 `npx`가 필요합니다. 프로젝트 디렉터리에서 다음 명령을 실행하고, 설치할 스킬과 에이전트를 선택하세요.

```sh
npx skills add gh-shin/skills
```

기본 설치 범위는 현재 프로젝트입니다. 목록 확인, 개별 스킬 선택, 사용자 전체 범위 설치에는 다음 옵션을 사용하세요.

```sh
# 설치 가능한 스킬 확인
npx skills add gh-shin/skills --list

# report-polish를 Codex 프로젝트에 설치
npx skills add gh-shin/skills --skill report-polish --agent codex

# 모든 스킬을 Codex 사용자 범위에 설치
npx skills add gh-shin/skills --skill '*' --agent codex --global
```

여러 에이전트를 지정하려면 `--agent` 옵션을 반복할 수 있습니다. 자세한 옵션은 [Skills CLI 문서](https://github.com/vercel-labs/skills#readme)를 참고하세요.

수동 설치가 필요한 경우 스킬 디렉터리 전체를 사용하는 에이전트의 스킬 폴더로 복사하세요. 예를 들어 Codex에서는 `report-polish/`를 `~/.agents/skills/report-polish/`에, `tech-report/`를 `~/.agents/skills/tech-report/`에 복사합니다. `tech-report`는 `references/markdown-html.md`도 함께 포함해야 합니다.

## 사용 예시

```text
$report-polish 아래 글을 사실·수치·조건을 유지하면서 개조식 보고서로 정리해 주세요.

[원문]
여기에 정리할 원문을 입력하세요.
```

이 저장소의 [LICENSE](LICENSE)는 Apache-2.0입니다.
