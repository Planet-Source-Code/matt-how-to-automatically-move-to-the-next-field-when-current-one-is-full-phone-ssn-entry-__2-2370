<div align="center">

## How to automatically move to the next field when current one is full \( phone, ssn entry, etc\)


</div>

### Description

Allows you to auto advance to the next field when the user fills up the current field with data. Great for entering phone or social security numbers that are broken out into their seperate fields (i.e.: area code, exchange, phone number) so the user doesn't have to tab to the next entry point.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Matt](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/matt.md)
**Level**          |Beginner
**User Rating**    |4.5 (18 globes from 4 users)
**Compatibility**  |
**Category**       |[Forms Validation Processing](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/forms-validation-processing__2-76.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/matt-how-to-automatically-move-to-the-next-field-when-current-one-is-full-phone-ssn-entry-__2-2370/archive/master.zip)





### Source Code

```
<head>
<script language="JavaScript">
<!--
function KeyUp(what,e,maxlen,action) {
 // *******************************************************
 // Input: what = the object in question
 //     e = the event of the object
 //     maxlen = maximum number of characters expected
 //     action = what to do when the maxlen is reached
 // *******************************************************
 // *
 // Netscape users
 if (document.layers) {
  if (e.target.value.length >= maxlen)
   eval(action);
 }
 // IE users
 else if (document.all) {
  if (what.value.length > maxlen-1)
   eval(action);
 }
}
//-->
</script>
</head>
<body>
<form>
 Social Security Number:<br>
 <input type="text" name="text1" size="3" maxlength="3" onKeyUp="KeyUp(this,event,3,'what.form.text2.focus()')"> -
 <input type="text" name="text2" size="2" maxlength="2" onKeyUp="KeyUp(this,event,2,'what.form.text3.focus()')"> -
 <input type="text" name="text3" size="4" maxlength="4">
</form>
</body>
```

