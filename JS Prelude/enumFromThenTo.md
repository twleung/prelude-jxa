```js
// enumFromThenTo :: Enum a => a -> a -> a -> [a]
const enumFromThenTo = (x1, x2, y) =>
    ('number' !== typeof x1 ? (
        enumFromThenToChar
    ) : enumFromThenToInt)
    .apply(null, [x1, x2, y]);
```