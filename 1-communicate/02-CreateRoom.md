# CreateRoom

방을 만듭니다.

## 요청 패킷

```typescript
interface RequestPacket {
  kind: "create-room";
  body: {
    gameType: GameType;
    options: object | undefined;
  };
}
```

- 게임 타입별로 필요한 옵션을 받습니다.
- 게임별로 옵션 규격은 다릅니다.

## 응답 패킷

```typescript
type ErrorKind = "not-allowed";
interface OkBody {}

interface ResponsePacket {
  ok: boolean;
  kind: "create-room";
  body: OkBody | Error<ErrorKind>;
}
```
