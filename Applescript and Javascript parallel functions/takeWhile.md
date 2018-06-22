```applescript
-- takeWhile :: (a -> Bool) -> [a] -> [a]
```

```js
// takeWhile :: (a -> Bool) -> [a] -> [a]
const takeWhile = (p, xs) => {
    let i = 0;
    const lng = xs.length;
    while ((i < lng) && p(xs[i])) (i = i + 1);
    return xs.slice(0, i);
};
```