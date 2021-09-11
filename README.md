# Auto Type to Screen
- Automatically work on computer
- Script base
- **WPF** for ui design


## Requirement
- re
- time
- pyautogui
- pyperclick
- os (flush CLI, Path)
- dotnet environment (Optional, can simply use demo.py)




# Auto Script

## System cmd:
```
<CMD> <sec or space>;
```
- commands for interpreter
1. **pause**
2. **gain_mouse_l**
    - loop to sequential gain mouse position
    - as an auxiliary tools for mouse cmd
3. **gain_mouse**
4. **gain_string**
## Mouse cmd:
```
<CMD> <x>, <y>;
```
- commands for mouse function
- Must provide **X, Y**.
1. **click**
2. **move_to**
## Keyboard cmd:
### Press Command
```
<press_CMD> <key or specific word>
press enter;
keydown backspace;
keyup backspace;
```
- specific word: 'enter', 'ctrl'
- **MIND: IF USE KEYDOWN, THEN MUST USE KEYUP BEFORE THE SCRIPTS!!!!!**
1. **press**
2. **keydown**
3. **keyup**
### Other Command
1. **hotkey**: for combinational key press
    ```
    hotkey <key1> <key2>
    # ex
    hotkey ctrl, c;
    ```
2. **write**: for input on keyboard
    ```
    write meg=<messages>;
    # ex
    write meg=Hello World!!!;
    ```
    - if want to input several lines, leave empty on meg, then a function will be executed to accept the article.



# Manual (for demo.py)
![comlex_work](https://github.com/lyz508/Auto-Operation-on-Computer/blob/master/resources/auto_show.gif)
- Choose Mode:
    1. Simple Type      
    2. Read Script
## Simple Type
```
- Basic use of auto click and input
- Type to specified position
- can set loop **times, interval, character** between loop.
```
0. Full process
    - Specified -> Input Message -> Type
1. Type with current settings
2. Change Settings
3. Show settings
4. Save current settings
    - default file name: setting.txt
5. Load formor settings
6. Back.
## Script
- Read Script File
0. Default script name (autoScript.txt)
1. Enter script name
2. Show avalible
    - show avalible files in current directory
3. Back.


# Update & Schedule
## Update
### 2021.8.22
- Complete a simple intepreter, which can deal with commands about mouse action and keyboard action.
- Change repository name: **AutoTypeToScreen** -> **Auto-Operation-on-Computer**
- Update detailed README
### 2021.8.23
- Add MVC for gui
    - M: libs.translator
    - V: autoViewer.csproj
    - C: autoController.py
- with WPF
- reformat README

## Schedule
![WPF_example](https://github.com/lyz508/Auto-Operation-on-Computer/blob/master/resources/WPF_example.gif)
### ~~Update Record function~~
- scheduled date: 2021.8.21
- Will be able to record the actions
- can afford complex work
- **Complete: 2021.8.22**
### Loop Support
- scheduled date: 2021.8.22
- Will support loop in scripts
### Combinational & Coordination on commands
- scheduled date: 2021.8.22
- will support mouse drag
### Multiple on Write Input
- scheduled date: 2021.8.22
- Problem:
    - when using repr(), colon wont be specified by re expression
    - using temp solution -> call handler function (read_message())
- Expected Solution
    - Optimized re exp.