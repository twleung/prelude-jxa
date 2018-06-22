```applescript
-- The 'isSortedBy' function returns true iff the predicate returns true
-- for all adjacent pairs of elements in the list.
```

```applescript
-- isSortedBy :: (a -> a -> Bool) -> [a] -> Bool
```

```js
// The 'isSortedBy' function returns true iff the predicate returns true
// for all adjacent pairs of elements in the list.
```

```js
// isSortedBy :: (a -> a -> Bool) -> [a] -> Bool
const isSortedBy = (cmp, xs) =>
    xs.length < 2 || all(x => x < 1, zipWith(cmp, xs, tail(xs)));
```