```applescript
-- Instance for lists only here

-- e.g. replicateM(3, {1, 2})) -> 
-- {{1, 1, 1}, {1, 1, 2}, {1, 2, 1}, {1, 2, 2}, {2, 1, 1}, 
--  {2, 1, 2}, {2, 2, 1}, {2, 2, 2}}
```

```applescript
-- replicateM :: Int -> [a] -> [[a]]
```

```js
// Instance for lists (arrays) only here
```

```js
// replicateM :: Int -> [a] -> [[a]]
const replicateM = (n, xs) => {
    const loop = x => x <= 0 ? [
        []
    ] : liftA2(cons, xs, loop(x - 1));
    return loop(n);
};
```