# 패킷 구조

TypeScript를 주력으로 사용하는 다락방 팀이므로, 문서 속 JSON 규격은 TypeScript 문법으로 서술합니다.

## 클라이언트 바운드 패킷

모든 클라이언트 바운드 패킷은 다음 구조를 따릅니다.

```typescript
type PacketKind = string;
type PacketBody = object;

interface ClientPacket {
  kind: PacketKind;
  body: PacketBody;
}
```

## 서버 바운드 패킷

모든 서버 바운드 패킷은 다음 구조를 따릅니다.

```typescript
type PacketKind = string;
type PacketBody = object;
type Error<ErrorKind extends string> = {
  kind: ErrorKind;
  description: string | undefined;
};

interface ServerPacket {
  ok: boolean;
  kind: PacketKind;
  body: PacketBody | Error<string>;
}
```
