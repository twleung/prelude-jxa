```js
// TupleN :: a -> b ...  -> (a, b ... )
function TupleN() {
    const
        args = Array.from(arguments),
        lng = args.length;
    return lng > 1 ? Object.assign(
        args.reduce((a, x, i) => Object.assign(a, {
            [i]: x
        }), {
            type: 'Tuple' + (2 < lng ? lng.toString() : ''),
            length: lng
        })
    ) : args[0];
};
```