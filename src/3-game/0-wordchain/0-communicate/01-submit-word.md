# submit-word

단어를 제시합니다.

## 요청 패킷

```typescript
interface RequestPacket {
  kind: "word-chain:submit-word";
  body: {
    word: string;
  };
}
```

## 응답 패킷

```typescript
type ErrorKind = "not-your-turn" | "invalid";
interface OkBody {}

interface ResponsePacket {
  ok: boolean;
  kind: "goto";
  body: OkBody | Error<ErrorKind>;
}
```
