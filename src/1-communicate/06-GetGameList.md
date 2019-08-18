# GetGameList

서버가 제공하는 게임 목록을 가져옵니다.

## 요청 패킷

```typescript
interface RequestPacket {
  kind: "get-game-list";
  body: {
    type: GameType;
  };
}
```

## 응답 패킷

```typescript
type ErrorKind = "not-exists";
interface OkData {
  gameList: Game[];
}

interface ResponsePacket {
  ok: boolean;
  kind: "get-game-list";
  body: OkData | Error<ErrorKind>;
}
```
