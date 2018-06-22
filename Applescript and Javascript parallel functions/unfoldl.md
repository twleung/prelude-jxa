```applescript
-- > unfoldl (\b -> if b == 0 then Nothing else Just (b, b-1)) 10
-- > [1,2,3,4,5,6,7,8,9,10]
```

```applescript
-- unfoldl :: (b -> Maybe (a, b)) -> b -> [a]
```

```js
// (x => Maybe [value, remainder] -> initial value -> values
```

```js
// unfoldl :: (b -> Maybe (a, b)) -> b -> [a]
const unfoldl = (f, v) => {
    let xs = [];
    return (
        until(
            mb => mb.Nothing,
            mb => (
                xs = [mb.Just[1]].concat(xs),
                f(mb.Just[1])
            ), Just(Tuple(v, v))
        ),
        xs.slice(1)
    );
};
```