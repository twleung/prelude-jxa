```applescript
-- sqrt :: Num -> Num
on sqrt(n)
    if n ≥ 0 then
        n ^ (1 / 2)
    else
        missing value
    end if
end sqrt
```

```js
// sqrt :: Num -> Num
const sqrt = n =>
    (0 <= n) ? Math.sqrt(n) : undefined;
```