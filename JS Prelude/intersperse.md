```js
// intersperse(0, [1,2,3]) -> [1, 0, 2, 0, 3]
```

```js
// intersperse :: a -> [a] -> [a]
// intersperse :: Char -> String -> String
const intersperse = (sep, xs) => {
    const bool = 'string' === typeof xs;
    return xs.length > 1 ? (
        (bool ? concat : x => x)(
            (bool ? (
                xs.split('')
            ) : xs)
            .slice(1)
            .reduce((a, x) => a.concat([sep, x]), [xs[0]])
        )) : xs;
};
```