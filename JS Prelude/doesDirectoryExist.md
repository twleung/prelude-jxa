```js
// doesDirectoryExist :: FilePath -> IO Bool
const doesDirectoryExist = strPath => {
    const ref = Ref();
    return $.NSFileManager.defaultManager
        .fileExistsAtPathIsDirectory(
            $(strPath)
            .stringByStandardizingPath, ref
        ) && (1 === ref[0]);
};
```