# get-room

방 정보를 가져옵니다.

## 요청 패킷

```typescript
interface RequestPacket {
  kind: "get-room";
  body: {
    roomId: RoomId;
  };
}
```

## 응답 패킷

```typescript
type ErrorKind = "not-exists";
interface OkData {
  room: Room;
}

interface ResponsePacket {
  ok: boolean;
  kind: "get-room";
  body: OkData | Error<ErrorKind>;
}
```
