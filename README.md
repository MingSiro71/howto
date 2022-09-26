# howto
Memorize and lookup knowredges that are hard to remember, such as complicated docker command, on YOUR TERMINAL.

## Instlation (recomended that clone on your account's root directory)
1. Clone sources
    ```
    git clone https://github.com/MingSiro71/howto.git
    ```
2. Change bin file to 755
    ```
    chmod 755 ./howto/bin/*
    ```
3. Add howto's bin directory to $PATH
    If you install source into your HOME directory, this will work.
    ```
    'export PATH=${PATH}:${HOME}/howto/bin' >> ~/.bashrc
    source .bashrc
    ```
    Please replace ".bashrc" to ".zshrc" if you use zsh, or some other setting file for your shell. 

## Memorize comamnd
    Use "theway" and you will asked how to do it. Type knowledge to keep then type "q" at the first character of the new line and type enter to finish. 
    ```
    theway do something
    > type knowledge (finish with "q"):
    my command
    q
    > remember new knowledge: do something

    my command    
    ```
### private knowledge
    with option "-p", you can stock knowledge as private. Private knowledge will avoid tracking by git so as not to shared though you push your knowledge commit.
    ```
    theway -p do something
    ```

    Private knowledges are prior to others when you use "howto" to lookup.

## Lookup comamnd
    Use "howto" with what you want to ask.
    ```
    howto do something
    > my command
    ```

### Ambiguous search
    With "-a" or "--ambiguous", you can search knowlege by word or the part of it.
    ```
    howto do some
    > available knowledges:
    > do something
    ```

### Copy to clipboard
    With "-c" or "--copy", it copies onto your clipboad instead of showing on terminal.
    ```
    howto -c do something
    ```
    No output is shown. Knowledge is on ready to paste.
    * This option works mac OS (with pdcopy) or windows (& wsl, clip.exe is available from termninal).
