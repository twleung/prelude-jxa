```js
// mappendTuple (<>) :: (a, b) -> (a, b) -> (a, b)
const mappendTuple = (t, t2) =>
    Tuple(mappend(t[0], t1[0]), mappend(t[1], t1[1]));
```