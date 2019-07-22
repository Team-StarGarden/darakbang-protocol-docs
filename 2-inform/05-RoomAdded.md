# RoomAdded

누군가가 방을 만들었음을 공지합니다.

```typescript
interface InformPacket {
  ok: true;
  kind: "room-added";
  body: {
    roomId: RoomId;
  };
}
```
