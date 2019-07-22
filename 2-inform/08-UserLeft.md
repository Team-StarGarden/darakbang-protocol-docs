# UserLeft

사용자가 퇴장하였음을 공지합니다.

```typescript
interface InformPacket {
  ok: true;
  kind: "user-left";
  body: {
    user: UserId;
  };
}
```
