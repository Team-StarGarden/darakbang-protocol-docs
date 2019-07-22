# Goto

메인 페이지, 게임 로비, 게임 방으로 이동합니다.

## 요청 패킷

```typescript
type GotoRoom = {
  game: GameType;
  room: RoomId;
};
type GotoGameLobby = {
  game: GameType;
};
type GotoMain = {};

interface RequestPacket {
  kind: "goto";
  body: GotoRoom | GotoGameLobby | GotoMain;
}
```

- `GotoMain` 규격에 맞으면 메인 페이지로 이동합니다.
- `GotoGameLobby` 규격에 맞으면 게임 로비까지 이동합니다.
- `GotoRoom` 규격에 맞으면 게임 방까지 이동합니다.

## 응답 패킷

```typescript
type ErrorKind = "is-room-full" | "unknown";
interface OkBody {}

interface ResponsePacket {
  ok: boolean;
  kind: "goto";
  body: OkBody | Error<ErrorKind>;
}
```
