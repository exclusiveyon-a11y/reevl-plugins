# Reevl 플러그인 마켓플레이스

AI 도구에서 **한국 아파트 데이터**를 바로 조회하기 위한 플러그인 모음입니다.

전국 아파트 약 45,000개의 실거래 시세·전세가율·거래량·입지 점수와
리블 AI 가격 예측을 공공데이터 기반으로 제공합니다.

## 설치 — Claude Code

```
/plugin marketplace add exclusiveyon-a11y/reevl-plugins
/plugin install reevl@reevl
```

설치 후 `/reload-plugins`가 필요하다고 하면 실행해 주세요.

## 들어 있는 플러그인

| 플러그인 | 내용 |
|---|---|
| [`reevl`](./reevl) | 리블 MCP 서버(도구 4종) + 한국 부동산 조회 스킬 |

## MCP 서버를 직접 연결하려면

플러그인 없이 MCP 서버만 붙일 수도 있습니다.

```
claude mcp add --transport http reevl https://reevl.co.kr/api/mcp
```

인증이 필요 없는 공개 읽기 전용 엔드포인트입니다.
Claude Code 외의 MCP 클라이언트도 같은 주소로 연결합니다 —
프로토콜은 Streamable HTTP이며 구버전 클라이언트도 함께 지원합니다.

## 도구

- **`describe_fields`** — 쓸 수 있는 모든 축과 **단위**, 값 분포, 시도별 단지 수
- **`search_apartments`** — 지역·가격·브랜드·시공사·세대수·전세가율·AI예측 조건 검색
- **`get_apartment`** — 단지 하나의 전 축 상세
- **`list_articles`** — 리블이 발행한 부동산 브리핑 목록

## 주의

**참고용 통계입니다.** 투자 자문이나 중개가 아니며, 실제 거래 판단의 책임은
이용자에게 있습니다. 모든 응답에 출처와 갱신일이 함께 반환됩니다.

## 데이터 출처

국토교통부 실거래가, 한국부동산원, K-apt(공동주택관리정보시스템),
KOSIS, 한국은행 ECOS, 국토교통부 V-World 등 공공데이터.

## 라이선스

플러그인 구성 파일은 [MIT](./LICENSE).
데이터 이용은 [리블 이용약관](https://reevl.co.kr/terms)을 따릅니다.

리블 · <https://reevl.co.kr> · [MCP 안내](https://reevl.co.kr/mcp)
