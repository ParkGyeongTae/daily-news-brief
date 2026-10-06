# Daily News Brief

매일 아침 6시(KST)에 한국·미국 뉴스, 커뮤니티 화제, AI, 데이터 소식을 모아 한국어로 요약하고 Slack `#daily-news-brief` 채널에 게시하는 Claude Code 루틴이다.

## 구성

| 파일 | 역할 |
|---|---|
| `AGENTS.md` | 루틴의 유일한 지시서. 수집 범위, 소스, 중복 방지, Slack 메시지 형식, 실행 절차를 정의한다 |
| `CLAUDE.md` | `AGENTS.md`를 가리키는 심볼릭 링크. Claude Code가 지시서를 자동으로 읽게 한다 |

## 실행 환경

- **스케줄**: Claude Code 루틴(`/schedule`)으로 매일 06:00 KST에 실행
- **필요한 커넥터**: Slack (채널 읽기·메시지 게시), WebSearch
- **게시 채널**: `#daily-news-brief` (ID `C0C6NRNGE81`)

## 결과물

채널에 부모 메시지("오늘의 핵심") 1개를 올리고, 섹션별 상세 내용은 그 스레드 답글로 게시한다.
형식과 규칙을 바꾸려면 `AGENTS.md`를 수정한다.
