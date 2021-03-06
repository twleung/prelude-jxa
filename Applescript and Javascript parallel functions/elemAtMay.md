```applescript
-- If x is a Dictionary then reads the Int as an index
-- into the lexically sorted keys of the Dict, 
-- returning a Maybe (Key, Value) pair.
-- If x is a list, then return a Maybe a 
-- (In either case, returns Nothing for an Int out of range)
```

```applescript
-- elemAtMay :: Int -> Dict -> Maybe (String, a)
-- elemAtMay :: Int -> [a] -> Maybe a
on elemAtMay(i, x)
    set bln to class of x is record
    if bln then
        set ks to keys(x)
        if i ≤ |length|(ks) then
            set k to item i of sort(ks)
            script pair
                on |λ|(v)
                    Just(Tuple(k, v))
                end |λ|
            end script
            bindMay(lookup(k, x), pair)
        end if
    else
        if i ≤ |length|(x) then
            Just(item i of x)
        else
            Nothing()
        end if
    end if
end elemAtMay
```

```js
// If x is a dictionary, then the Int is read as an 
// index into the lexically sorted keys of the Dict, 
// returning a Maybe (Key, Value) pair.
// If x is a list, then returns a Maybe a.
// (In either case, returns Nothing for an Int out of range)
```

```js
// elemAtMay :: Int -> Dict -> Maybe (String, a)
// elemAtMay :: Int -> [a] -> Maybe a
const elemAtMay = (i, x) => {
    const
        bln = Array.isArray(x),
        k = bln ? i : Object.keys(x)
        .sort()[i],
        v = x[k];
    return undefined !== v ? (
        Just(bln ? v : Tuple(k, v))
    ) : Nothing();
};
```