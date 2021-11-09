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

## code-gen-lib localization module parameters with generating outside the run directory folder -ofp for full path
```python
sh localization-swift.sh -p modules/localization-swift/Localizable.strings -ofp /Users/***/Desktop/localization


generated files ...
/Users/***/Desktop/localization/Localization-General+Extensions.swift
/Users/***/Desktop/localization/Localization-Components+Extensions.swift
/Users/***/Desktop/localization/Localization-Pages+Extensions.swift
/Users/***/Desktop/localization/Localization-Shared+Extensions.swift
/Users/***/Desktop/localization/Localization-PushNotification+Extensions.swift
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

## HomeBrew localization-swift brew run permission denied solve
```python
#1.2 current version
$ sudo chmod 755 /usr/local/Cellar/localization-swift/1.2/libexec/localization-swift.sh

```

## HomeBrew localization-swift run on brew installed path without global env 
```python
#1.2 current version
$ sh /usr/local/Cellar/localization-swift/1.2/libexec/localization-swift.sh -p Localizable.strings

```
## Run Action Script at Use to XCODE Build Phase  --localization-swift
The recommended way to use Localization-swift is to create a "Run Script" Build Phase (Xcode > Project > Targets > Your build target > Build Phases > New Run Script Phase)
```python
# Type a script or drag a script file from your workspace to insert its path.
set -x
 
# Get base path to project
BASE_PATH="$PROJECT_DIR/$PROJECT_NAME"
LOCALIZABLE_FILE="Localizable.strings"
LOCALIZABLE_FILE_PATH="$BASE_PATH/$LOCALIZABLE_FILE"
OUTPUT_FILE_PATH="$BASE_PATH/Localization"

echo $LOCALIZABLE_FILE_PATH

LOCALIZABLE_COMMAND="sh /usr/local/Cellar/localization-swift/1.2/libexec/localization-swift.sh -fp "$LOCALIZABLE_FILE_PATH" -ofp "$OUTPUT_FILE_PATH
$LOCALIZABLE_COMMAND

```