```js
-- use framework "Foundation"
-- use scripting additions
```

```js
-- lookup :: Eq a => a -> Container -> Maybe b
```

```js
// lookup :: Eq a => a -> Container -> Maybe b
const lookup = (k, m) =>
    (Array.isArray(m) ? (
        lookupTuples
    ) : lookupDict)(k, m);
```