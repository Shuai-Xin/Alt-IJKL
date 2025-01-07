# Alt-IJKL
An AutoHotKey(AHK) script to map Alt+IJKL to arrow key (↑,←,↓,→) with other convenient features.

因為加上其他組合鍵（比如説額外再按下 Control，變成 Ctl+Alt+J）後，AHK 會當作全新的組合情形來判斷，所以每種組合都要詳細定義行爲。

# How to use
安裝 AutoHotKey，使用以下 script，執行！

# The script
```
#Requires AutoHotkey v2.0


; This script is made by Shuai. 
; For more information, please visit https://github.com/Shuai-Xin/Alt-IJKL/


; Define Alt+I/K/J/L ------------------> Arrow key
!i::Send("{Up}")      ; Alt+I -> up
!k::Send("{Down}")    ; Alt+K -> down
!j::Send("{Left}")    ; Alt+J -> left
!l::Send("{Right}")   ; Alt+L -> right


; Define Shift+Alt+I/K/J/L ------------> Shift+Arrow
+!i::Send("+{Up}")      ; shift+up
+!k::Send("+{Down}")    ; shift+down
+!j::Send("+{Left}")    ; shift+left
+!l::Send("+{Right}")   ; shift+right


; Define Ctrl+Alt+J/K/L/I  ------------> Ctrl+Arrow
^!i::Send("^{Up}")      ; Ctrl+Alt+I -> Ctrl+up
^!k::Send("^{Down}")    ; Ctrl+Alt+K -> Ctrl+down
^!j::Send("^{Left}")    ; Ctrl+Alt+J -> Ctrl+left
^!l::Send("^{Right}")   ; Ctrl+Alt+L -> Ctrl+right


; Define Win+Alt+J/K/L/I  -------------> Win+Arrow
#!i::Send("#{Up}")      ; Win+Alt+I -> Win+up
#!k::Send("#{Down}")    ; Win+Alt+K -> Win+down
#!j::Send("#{Left}")    ; Win+Alt+J -> Win+left
#!l::Send("#{Right}")   ; Win+Alt+L -> Win+right


; Define Shift+Ctrl+Alt+J/K/L/I -------> Shift+Ctrl+Arrow
+^!i::Send("+^{Up}")      ; Shift+Ctrl+Alt+I -> Shift+Ctrl+up
+^!k::Send("+^{Down}")    ; Shift+Ctrl+Alt+K -> Shift+Ctrl+down
+^!j::Send("+^{Left}")    ; Shift+Ctrl+Alt+J -> Shift+Ctrl+left
+^!l::Send("+^{Right}")   ; Shift+Ctrl+Alt+L -> Shift+Ctrl+right


; Define Windows+Shift+Alt+J/K/L/I -----> Windows+Shift+Arrow
#+!i::Send("#+{Up}")      ; Windows+Shift+Alt+I -> Windows+Shift+up
#+!k::Send("#+{Down}")    ; Windows+Shift+Alt+K -> Windows+Shift+down
#+!j::Send("#+{Left}")    ; Windows+Shift+Alt+J -> Windows+Shift+left
#+!l::Send("#+{Right}")   ; Windows+Shift+Alt+L -> Windows+Shift+right


; Define Alt+U to Home, Alt+O to End.
!u::Send("{Home}")
!o::Send("{End}")


; Define Alt+Shift+U/O to Shift+Home/End.
+!u::Send("+{Home}")
+!o::Send("+{End}")
```
