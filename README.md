# code-gen-library - localization-swift module
code-gen-library - localization-swift module with Python bash script execute to localization swift files(struct and extension) by localization strings file


## using example
```python
sh code_gen_lib_example.sh
```

## code-gen-lib localization module parameters --info
```python
sh localization-swift.sh --info                                            
In the __init__  method of the Base class call child from : FileOperation
you can string file with under folder path -p
-p /string-file-path
you can string file with full path -fp
-fp /Users/***/Desktop/..
```


## code-gen-lib localization module parameters with full path -fp for strings file
```python
sh localization-swift.sh -fp /Users/***/Desktop/App/localization-swift/Localizable.strings


generated files ...
Localization-General+Extensions.swift
Localization-Components+Extensions.swift
Localization-Pages+Extensions.swift
Localization-Shared+Extensions.swift
Localization-PushNotification+Extensions.swift
```

## code-gen-lib localization module parameters  with sub path -p for strings file
```python
sh localization-swift.sh -p modules/localization-swift/Localizable.strings


generated files ...
Localization-General+Extensions.swift
Localization-Components+Extensions.swift
Localization-Pages+Extensions.swift
Localization-Shared+Extensions.swift
Localization-PushNotification+Extensions.swift
```

## code-gen-lib localization module parameters with generating inner folder -o for path
```python
sh localization-swift.sh -p modules/localization-swift/Localizable.strings -o localization


generated files ...
localization/Localization-General+Extensions.swift
localization/Localization-Components+Extensions.swift
localization/Localization-Pages+Extensions.swift
localization/Localization-Shared+Extensions.swift
localization/Localization-PushNotification+Extensions.swift
```

## HomeBrew localization-swift installation
The missing package manager for macOS.  Homebrew won’t install files outside its prefix, and you can place a Homebrew installation wherever you like.

After installed Homebrew, execute following commands
```python
$ brew install localization-swift --HEAD
```
For localization-swift installation, run the following command:

1.
```python
$ brew search oneframemobile/localization-swift/localization-swift
```

2.
```python
$ brew install localization-swift
```