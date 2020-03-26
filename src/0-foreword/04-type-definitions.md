# 타입 정의

공통으로 자주 나올 타입에 대한 정의입니다.

```typescript
// Aliases
export { GameCategory } from "darakbang-be/src/packet/common";

export type RoomId = number;
export type UserId = string;
export type char = string; // TypeScript doesn't support char type, it's just convention.

// Core Types
export interface Room {
  id: number;
  rules: GameRule[];
  players: {
    current: number;
    max: number;
  };
  canJoin: boolean;
}
export interface User {
  userId: number;
  displayName: string;
  tag: number;
}
export enum GameType {
  OnggiJonggi = '옹기종기',
  Wakjajiggeol = '왁자지껄',
}

export interface Game {
  category: GameCategory;
  type: GameType;
}

```
