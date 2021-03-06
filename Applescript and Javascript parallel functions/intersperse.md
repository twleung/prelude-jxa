```applescript
-- intersperse(0, [1,2,3]) -> [1, 0, 2, 0, 3]
```

```applescript
-- intersperse :: a -> [a] -> [a]
-- intersperse :: Char -> String -> String
on intersperse(sep, xs)
    set lng to length of xs
    if lng > 1 then
        set acc to {item 1 of xs}
        repeat with i from 2 to lng
            set acc to acc & {sep, item i of xs}
        end repeat
        if class of xs is string then
            concat(acc)
        else
            acc
        end if
    else
        xs
    end if
end intersperse
```

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