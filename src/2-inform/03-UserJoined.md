# UserJoined

사용자가 접속하였음을 공지합니다.

```typescript
interface InformPacket {
  ok: true;
  kind: "user-joined";
  body: {
    user: UserId;
  };
}
```
