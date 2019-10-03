# room-updated

어떤 방의 정보가 업데이트되었음을 공지합니다.

```typescript
interface InformPacket {
  ok: true;
  kind: "room-updated";
  body: {
    roomId: RoomId;
  };
}
```
