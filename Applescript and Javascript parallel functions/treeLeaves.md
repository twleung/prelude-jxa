```applescript
-- treeLeaves :: Tree -> [Tree]
on treeLeaves(oNode)
    script go
        on |λ|(x)
            set lst to nest of x
            if 0 < length of lst then
                concatMap(my treeLeaves, lst)
            else
                {x}
            end if
        end |λ|
    end script
    |λ|(oNode) of go
end treeLeaves
```

```js
// treeLeaves :: Tree -> [Tree]
const treeLeaves = tree => {
  const nest = tree.nest;
  return (0 < nest.length) ? (
    concatMap(treeLeaves, nest)
  ) : [tree];
};
```