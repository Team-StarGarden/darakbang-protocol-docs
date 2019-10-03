# turn-changed

턴이 `target` 에게 넘어갔음을 알립니다.

```typescript
interface InformPacket {
  ok: true;
  kind: "word-chain:turn-changed";
  body: {
    target: UserId;
  };
}
```
