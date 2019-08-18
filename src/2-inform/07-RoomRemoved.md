# RoomRemoved

어떤 방이 삭제되었음을 공지합니다.

```typescript
interface InformPacket {
  ok: true;
  kind: "room-removed";
  body: {
    roomId: RoomId;
  };
}
```
