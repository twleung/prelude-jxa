```applescript
-- Ordering  :: (-1 | 0 | 1)
```

```applescript
-- compare :: a -> a -> Ordering
```

```js
// compare :: a -> a -> Ordering
const compare = (a, b) => a < b ? -1 : (a > b ? 1 : 0);
```