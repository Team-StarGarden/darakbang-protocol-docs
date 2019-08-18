# GetUser

특정 사용자에 대한 정보를 가져옵니다.

## 요청 패킷

```typescript
interface RequestPacket {
  kind: "get-user";
  body: {
    id: UserId;
  };
}
```

## 응답 패킷

```typescript
type ErrorKind = "invalid-id";
interface OkData {
  user: User;
}

interface ResponsePacket {
  ok: boolean;
  kind: "get-user";
  body: OkData | Error<ErrorKind>;
}
```
