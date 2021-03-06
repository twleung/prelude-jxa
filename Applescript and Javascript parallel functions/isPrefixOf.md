```applescript
-- isPrefixOf takes two lists or strings and returns 
--  true if and only if the first is a prefix of the second.
```

```applescript
-- isPrefixOf :: [a] -> [a] -> Bool
-- isPrefixOf :: String -> String -> Bool
on isPrefixOf(xs, ys)
    script go
        on |λ|(xs, ys)
            set intX to length of xs
            if intX < 1 then
                true
            else if intX > length of ys then
                false
            else if class of xs is string then
                (offset of xs in ys) = 1
            else
                set {xxt, yyt} to {Just of uncons(xs), Just of uncons(ys)}
                ((|1| of xxt) = (|1| of yyt)) and |λ|(|2| of xxt, |2| of yyt)
            end if
        end |λ|
    end script
    go's |λ|(xs, ys)
end isPrefixOf
```

```js
// isPrefixOf takes two lists or strings and returns 
// true iff the first is a prefix of the second.
```

```js
// isPrefixOf :: [a] -> [a] -> Bool
// isPrefixOf :: String -> String -> Bool
const isPrefixOf = (xs, ys) => {
    const go = (xs, ys) => {
        const intX = xs.length;
        return 0 < intX ? (
            ys.length >= intX ? xs[0] === ys[0] && go(
                xs.slice(1), ys.slice(1)
            ) : false
        ) : true;
    };
    return 'string' !== typeof xs ? (
        go(xs, ys)
    ) : ys.startsWith(xs);
};
```