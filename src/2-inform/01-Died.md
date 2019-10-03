# died

방/게임 로비/서버 등이 죽기 전, 플레이어를 다른 곳으로 보냅니다.

```typescript
type SendTo = "game-lobby" | "server" | "error";
type Message = string;

interface InformPacket {
  ok: true;
  kind: "died";
  body: {
    sendTo: SendTo;
    message: Message;
  };
}
```

- `SendTo` 에서 명시한 대로 게임 로비, 서버, 에러 페이지 중 한 곳으로 보냅니다.
