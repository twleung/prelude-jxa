```applescript
use framework "Foundation"
-- File name template -> string data -> temporary path
-- (Random digit sequence inserted between template base and extension)
```

```applescript
-- writeTempFile :: String -> String -> IO FilePath
on writeTempFile(template, txt)
    set strPath to (current application's ¬
        NSTemporaryDirectory() as string) & ¬
        takeBaseName(template) & ¬
        text 3 thru -1 of ((random number) as string) & ¬
        takeExtension(template)
    -- Effect
    writeFile(strPath, txt)
    -- Value
    strPath
end writeTempFile
```

```js
// File name template -> string data -> IO temporary path
```

```js
// writeTempFile :: String -> String -> IO FilePath
const writeTempFile = (template, txt) => {
    const
        strPath = ObjC.unwrap($.NSTemporaryDirectory()) +
        takeBaseName(template) + Math.random()
        .toString()
        .substring(3) + takeExtension(template);
    return (writeFile(strPath, txt), strPath);
};
```