
```ts
type MyAwaited<T> = T extends Promise<infer S> ? MyAwaited<S> : T
```