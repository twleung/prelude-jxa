```js
// floor :: Num -> Int
const floor = x => {
    const
      nr = properFraction(x),
      n = nr[0];
    return 0 > nr[1] ? n - 1 : n;
};
```