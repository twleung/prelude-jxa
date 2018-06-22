```applescript
-- Applied to a predicate and a list, 
-- |any| returns true if at least one element of the 
-- list satisfies the predicate.
```

```applescript
-- any :: (a -> Bool) -> [a] -> Bool
```

```js
// | True if any contained element satisfies the predicate.
```

```js
// any :: (a -> Bool) -> [a] -> Bool
const any = (p, xs) => xs.some(p);
```