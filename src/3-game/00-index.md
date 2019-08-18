# 게임 패킷

각 게임은 서로 다른 콘텐츠를 전하기 때문에 동일한 규격으로 모든 게임을 담을 수는 없습니다.
따라서 게임 진행 중에 사용하는 패킷은 아무리 공통으로 관리할 수 있어도 별개의 표준으로 작성합니다.

## 형식

각 게임은 인덱스 페이지에 다음 형식을 따릅니다.
치환해야할 플레이스 홀더 값은 중괄호 쌍으로 나타냅니다.
플레이스 홀더 값에 들어가는 값이 제한적인 경우, `|`로 묶어 나타냅니다.

```md
`{게임에 대한 간략한 설명}`

| 속성         | 값                                        |
| ------------ | ----------------------------------------- |
| 한국어 명칭  | `{플레이스홀더}`                          |
| 영어 명칭    | `{플레이스홀더}`                          |
| 네임스페이스 | `{플레이스홀더}`                          |
| 단계         | `{프로토콜 구성 | 구현 시작 | 구현 완료}` |
| 공개         | `{공개 예정 | 공개 중 | 공개 중단}`       |
```