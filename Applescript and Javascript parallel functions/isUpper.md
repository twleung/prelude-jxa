```applescript
-- isUpper :: Char -> Bool
on isUpper(c)
    set d to (id of c) - 65 -- id of "A"
    d ≥ 0 and d < 26
end isUpper
```

```js
// isUpper :: Char -> Bool
const isUpper = c =>
    /[A-Z]/.test(c);
```