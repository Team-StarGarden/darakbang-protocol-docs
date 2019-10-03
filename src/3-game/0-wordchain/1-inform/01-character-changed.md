# character-changed

끝 문자가 변경되었음을 알립니다.

```typescript
interface InformPacket {
  ok: true;
  kind: "word-chain:character-changed";
  body: {
    character: char;
  };
}
```
