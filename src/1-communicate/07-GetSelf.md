# GetSelf

자기 자신에 대한 정보를 가져옵니다.

## 요청 패킷

```typescript
interface RequestPacket {
  kind: "get-self";
  body: {};
}
```

## 응답 패킷

```typescript
type ErrorKind = "invalid-session";
interface OkData {
  self: User;
}

interface ResponsePacket {
  ok: boolean;
  kind: "get-self";
  body: OkData | Error<ErrorKind>;
}
```
