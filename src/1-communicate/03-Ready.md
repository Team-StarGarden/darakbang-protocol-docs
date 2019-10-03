# ready

준비 상태를 변경합니다.

## 요청 패킷

```typescript
interface RequestPacket {
  kind: "ready";
  body: {
    status: boolean;
  };
}
```

## 응답 패킷

```typescript
type ErrorKind = "not-in-room";
interface OkBody {}

interface ResponsePacket {
  ok: boolean;
  kind: "ready";
  body: OkBody | Error<ErrorKind>;
}
```
