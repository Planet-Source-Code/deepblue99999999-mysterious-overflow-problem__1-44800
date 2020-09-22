<div align="center">

## Mysterious Overflow Problem


</div>

### Description

One day, I was performing calculation on numeric variables.I kept getting error message "Overflow" so I checked my variable declaration, it's declared as Long, but the operation of the two numeric values gave 2500. I was confused at first, finally I brought up MSDN help and discovered the solution.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[deepblue99999999](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/deepblue99999999.md)
**Level**          |Beginner
**User Rating**    |4.1 (29 globes from 7 users)
**Compatibility**  |VB 3\.0, VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0, VB Script, ASP \(Active Server Pages\) , VBA MS Access, VBA MS Excel
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__1-1.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/deepblue99999999-mysterious-overflow-problem__1-44800/archive/master.zip)





### Source Code

```
This will generate an error message "Overflow"
Sub Command1_Click()
Dim X As Long
X = 2000 * 350
End Sub
'This is the solution I got from MSDN.
Sub Command1_Click()
Dim X As Long
X = CLng(2000) * 350 Or
X = 2000 * CLng(350)
End Sub
```

