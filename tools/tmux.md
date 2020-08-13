### Main commands of tmux
1. Create a new session
    ```
    tmux new-session -s <sesstion name>
    ```
1. Create a new window:
    ```
    CTRL+b -> c (create)
    ```
1. Switch between windows:
    ```
    CTRL+b -> 0 (window id number)
    ```
1. Split window on two vertical windows:
    ```
    CTRL+b -> %
    ```
1. Scroll:
    ```
    Ctrl-b -> [ -> normal navigation keys to scroll around (eg. Up Arrow or PgDn)
    ```
    Press q to quit scroll mode.
1. Split window on two horisontal windows:
    ```
    CTRL+b -> "
    ```
 1. Switch between windows:
    ```
    CTRL+b -> left/rigth/up/down
    ```
1. Detach from session:
    ```
    CTRL+b -> d
    ```
1. Attach session:
    ```
    tmux attach -t <sesstion name>
    ```
1. Show tmux session list:
    ```
    tmux ls
    ```
1. Kill session:
    ```
    tmux kill-session
    ```

### Configure tmux
1. Activate mouse:
    ```
    echo "set -g mouse on" >> ~/.tmux.conf
    ```

   
### Links
1. [tmux video tutorial](https://www.youtube.com/playlist?list=PLAk6CfuV7hyq4NeNn8gJt8OEpPisPh_Fr)
1. [How to close a tmux session](https://superuser.com/questions/777269/how-to-close-a-tmux-session/777292)
