# Alt-IJKL
An AutoHotKey(AHK) script to map Alt+IJKL to arrow key (↑,←,↓,→) with other convenient features.

因為加上其他組合鍵（比如説額外再按下 Control，變成 Ctl+Alt+J）後，AHK 會當作全新的組合情形來判斷，所以每種組合都要詳細定義行爲。 

```
#Requires AutoHotkey v2.0


; 全局設置 Alt+I/K/J/L 為方向鍵
!i::Send("{Up}")      ; Alt+I -> 向上
!k::Send("{Down}")    ; Alt+K -> 向下
!j::Send("{Left}")    ; Alt+J -> 向左
!l::Send("{Right}")   ; Alt+L -> 向右


; 全局設置 Shift+Alt+I/K/J/L -> shift+方向鍵
+!i::Send("+{Up}")      ; shift+向上
+!k::Send("+{Down}")    ; shift+向下
+!j::Send("+{Left}")    ; shift+向左
+!l::Send("+{Right}")   ; shift+向右


; 顯式定義 Ctrl+Alt+J/K/L/I 為對應的方向鍵
^!i::Send("^{Up}")      ; Ctrl+Alt+I -> 向上
^!k::Send("^{Down}")    ; Ctrl+Alt+K -> 向下
^!j::Send("^{Left}")    ; Ctrl+Alt+J -> 向左
^!l::Send("^{Right}")   ; Ctrl+Alt+L -> 向右


; Shift+Ctrl+Alt+J/K/L/I -> Shift+Ctrl+方向鍵
+^!i::Send("+^{Up}")      ; Shift+Ctrl+Alt+I -> Shift+Ctrl+向上
+^!k::Send("+^{Down}")    ; Shift+Ctrl+Alt+K -> Shift+Ctrl+向下
+^!j::Send("+^{Left}")    ; Shift+Ctrl+Alt+J -> Shift+Ctrl+向左
+^!l::Send("+^{Right}")   ; Shift+Ctrl+Alt+L -> Shift+Ctrl+向右


; 定義 Windows+Alt+J/K/L/I -> Windows+方向鍵
#!i::Send("#{Up}")      ; Windows+Alt+I -> Windows+向上
#!k::Send("#{Down}")    ; Windows+Alt+K -> Windows+向下
#!j::Send("#{Left}")    ; Windows+Alt+J -> Windows+向左
#!l::Send("#{Right}")   ; Windows+Alt+L -> Windows+向右
```
