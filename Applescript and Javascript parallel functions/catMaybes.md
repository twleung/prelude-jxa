```applescript
-- catMaybes :: [Maybe a] -> [a]
on catMaybes(mbs)
    script emptyOrListed
        on |λ|(m)
            if Nothing of m then
                {}
            else
                {Just of m}
            end if
        end |λ|
    end script
    concatMap(emptyOrListed, mbs)
end catMaybes
```

```js
// catMaybes :: [Maybe a] -> [a]
const catMaybes = mbs =>
    concatMap(m => m.Nothing ? [] : [m.Just], mbs);
```