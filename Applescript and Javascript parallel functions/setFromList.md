```applescript
-- NB All names of NSMutableSets should be set to *missing value*
-- before the script exits.
-- ( scpt files can not be saved if they contain ObjC pointer values )
```

```applescript
-- setFromList :: Ord a => [a] -> Set a
on setFromList(xs)
    set ca to current application
    ca's NSMutableSet's ¬
        setWithArray:(ca's NSArray's arrayWithArray:(xs))
end setFromList
```

```js
// setFromList :: Ord a => [a] -> Set a
const setFromList = xs =>
    new Set(xs);
```