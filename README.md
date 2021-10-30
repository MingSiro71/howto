# howto: WSL version
Memolize commands which are complicated, long or hard to remember.
You can lookup them easily on your terminal.

This works only on WSL.
Please customize clipboard-concerning command
in Mac: "clip.exe" to "pbcopy"
in Linux: Ask google! :-P

## Instlation (recomended for your own workstation)
1. Make directory for howto
    ```
    cd ~
    mkdir -p howto/bin howto/lib
    ```
2. Copy this file into binary directory which you made
3. Change mode to 755
    ```
    chmod 755 howto/bin/howto
    ```
4. Add ${HOME}/howto/bin into $PATH
    ```
    echo "PATH=${PATH}:${HOME}/howto/bin" >> .bashrc
    source .bashrc
    ```

## Register your command
1. Make text file into howto/lib
    ```
    echo "my command" > ~/howto/lib/do-something
    # Or, use your favorite editor
    ```

## Remind comamnd
1. type howto command
    ```
    howto do-something
    > my command
    ```

## Copy command on your
1. type howto command with "c" option
    ```
    howto -c do-something
    # Nothing happened? From clipboard, paste into somewhere!
    ```
