## Configuring Qt Creator

1. Install Qt Creator:
    ```
    sudo apt install -y build-essential qtcreator clang-format
    ```
1. Set code style options:
    - Select **Help > About Plugins > C++ > Beautifier** to enable the plugin.
    - Select **Tools > Options... > Beautifier > Clang Format** to specify settings.
    - Select the **Use customized style** option, and then **Add** to define your own style.
        ```
        BasedOnStyle: Google
        IndentWidth: 4
        AllowShortFunctionsOnASingleLine: None
        BreakBeforeBinaryOperators: None
        ColumnLimit: 120
        ```
        ![](http://doc.qt.io/qtcreator/images/beautifier_editor.png, "")
1. Customize keyboard shortcut. Select **Tools > Options > Environment > Keyboard** and find where **ClangFormat > FormatFile** in the middle column, then click on it and press **Ctrl+Shift+L**.


## Links
1. [Beautifying Source Code](http://doc.qt.io/qtcreator/creator-beautifier.html)
1. [Clang-Format Style Options](http://clang.llvm.org/docs/ClangFormatStyleOptions.html)
1. [What is the shortcut to format code in Qt Creator?](https://stackoverflow.com/questions/37597117/what-is-the-shortcut-to-format-code-in-qt-creator)