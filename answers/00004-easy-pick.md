
# 00004-easy-pick

## Pick

픽 타입은 특정 타입에서 몇 개의 속성을 선택하여 타입을 정의

```typescript
interface Todo {
    title: string
    description: string
    completed: boolean
}

type MyPick<T, K extends keyof T> = {
    [P in K]: T[P]
}

// type TodoPreview = Pick<Todo, 'title' | 'completed'>
type TodoPreview = MyPick<Todo, 'title' | 'completed'>

const todo: TodoPreview = {
    title: 'Clean room',
    completed: false,
}
```
