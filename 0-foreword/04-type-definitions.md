# 타입 정의

공통으로 자주 나올 타입에 대한 정의입니다.

```typescript
// Aliases
export type GameType = string;
export type RoomId = number;
export type UserId = string;

// Core Types
export { Room } from "darakbang-fe/src/lib/room"; // *1
export { User } from "darakbang-fe/src/lib/user"; // *2
export { GameType, Game } from "darakbang-be/src/core/game"; // *3
```

- [\*1: darakbang-fe/src/lib/room](https://gitlab.com/Team-StarGarden/Darakbang/darakbang-fe/blob/master/src/lib/room.ts)
- [\*2: darakbang-fe/src/lib/user](https://gitlab.com/Team-StarGarden/Darakbang/darakbang-fe/blob/master/src/lib/user.ts)
- [\*3: darakbang-be/src/core/game](https://gitlab.com/Team-StarGarden/Darakbang/darakbang-be/blob/master/src/core/game.ts)
