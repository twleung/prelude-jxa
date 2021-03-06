```applescript
-- drop :: Int -> [a] -> [a]
-- drop :: Int -> String -> String
on drop(n, xs)
    set c to class of xs
    if c is not script then
        if c is not string then
            if n < length of xs then
                items (1 + n) thru -1 of xs
            else
                {}
            end if
        else
            if n < length of xs then
                text (1 + n) thru -1 of xs
            else
                ""
            end if
        end if
    else
        take(n, xs) -- consumed
        return xs
    end if
end drop
```

```js
// drop :: Int -> [a] -> [a]
// drop :: Int -> Generator [a] -> Generator [a]
// drop :: Int -> String -> String
const drop = (n, xs) =>
    Infinity > length(xs) ? (
        xs.slice(n)
    ) : (take(n, xs), xs);
```