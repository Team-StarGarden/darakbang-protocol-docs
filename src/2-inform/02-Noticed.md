# noticed

공지 사항을 전달합니다.

```typescript
type NoticeKind = "reboot" | "other";
type Message = string;

interface InformPacket {
  ok: true;
  kind: "noticed";
  body: {
    kind: NoticeKind;
    message: Message;
  };
}
```
