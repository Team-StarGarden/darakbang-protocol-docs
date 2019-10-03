# start-game

게임을 시작합니다.

## 요청 패킷

```typescript
interface RequestPacket {
  kind: "start-game";
  body: {};
}
```

## 응답 패킷

```typescript
type ErrorKind = "not-in-room" | "no-permission" | "not-full-ready";
interface OkData {}

interface ResponsePacket {
  ok: boolean;
  kind: "start-game";
  body: OkData | Error<ErrorKind>;
}
```
