<div align="center">

## A KeyCode to Strings Converter


</div>

### Description

It is a function that converts keycodes like those used in _KeyDown events, to strings like "Ctrl", "Alt", "F", "/", which are recognizable to the end-user. Great for game programmers.
 
### More Info
 
KeyCode as Integer

If the user presses Shift+3, the function will not return "#", but will return "3" instead. It also uses easily recognizable symbols to represent certain keys, e.g "~" instead of "`", "\" instead of "|", and "Pg Dn", "Enter", "Space", to represent other keys.

KeyStr as String

If a key inputted does not match with any of the strings listed, the string returned will be "!".


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Alexander Chia](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/alexander-chia.md)
**Level**          |Beginner
**User Rating**    |4.2 (25 globes from 6 users)
**Compatibility**  |VB 3\.0, VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[VB function enhancement](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/vb-function-enhancement__1-25.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/alexander-chia-a-keycode-to-strings-converter__1-4116/archive/master.zip)





### Source Code

```
Public Function KeyStr(KeyCode As Integer) As String
 'Copyright Alexander Chia Yan Sheng
 Select Case KeyCode
 Case 65 To 90
  KeyStr = Chr(KeyCode)
 Case 48 To 57
  KeyStr = Chr(KeyCode)
 Case 13
  KeyStr = "Enter"
 Case 9
  KeyStr = "Tab"
 Case 112 To 123
  KeyStr = "F" & LTrim(Str(KeyCode - 111))
 Case 27
  KeyStr = "Esc"
 Case 192
  KeyStr = "~"
 Case 187
  KeyStr = "="
 Case 189
  KeyStr = "-"
 Case 219
  KeyStr = "["
 Case 220
  KeyStr = "\"
 Case 221
  KeyStr = "]"
 Case 186
  KeyStr = ";"
 Case 222
  KeyStr = "'"
 Case 188
  KeyStr = ","
 Case 190
  KeyStr = "."
 Case 191
  KeyStr = "/"
 Case 16
  KeyStr = "Shift"
 Case 20
  KeyStr = "Caps Lock"
 Case 144
  KeyStr = "Num Lock"
 Case 145
  KeyStr = "Scr Lock"
 Case 17
  KeyStr = "Ctrl"
 Case 18
  KeyStr = "Alt"
 Case 32
  KeyStr = "Space"
 Case 45
  KeyStr = "Ins"
 Case 46
  KeyStr = "Del"
 Case 33
  KeyStr = "Pg Up"
 Case 34
  KeyStr = "Pg Dn"
 Case 8
  KeyStr = "Back"
 Case 36
  KeyStr = "Home"
 Case 35
  KeyStr = "End"
 Case 37
  KeyStr = "Left Arrow"
 Case 38
  KeyStr = "Up Arrow"
 Case 39
  KeyStr = "Right Arrow"
 Case 40
  KeyStr = "Down Arrow"
 Case 106
  KeyStr = "* [Num Pad]"
 Case 107
  KeyStr = "+ [Num Pad]"
 Case 111
  KeyStr = "/ [Num Pad]"
 Case 109
  KeyStr = "- [Num Pad]"
 Case Else
  KeyStr = "!"
 End Select
End Function
```

