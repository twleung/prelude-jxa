```applescript
-- Ordering :: ( LT | EQ | GT ) | ( -1 | 0 | 1 )
```

```applescript
-- mappendOrdering (<>) :: Ordering -> Ordering -> Ordering
```

```js
// mappendOrdering (<>) :: Ordering -> Ordering -> Ordering
const mappendOrdering = (a, b) => eqOrdering(EQ, a) ? b : a;
```