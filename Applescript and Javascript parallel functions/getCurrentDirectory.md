```applescript
-- getCurrentDirectory :: IO FilePath
```

```js
// getCurrentDirectory :: IO FilePath
const getCurrentDirectory = () =>
    ObjC.unwrap($.NSFileManager.defaultManager.currentDirectoryPath);
```