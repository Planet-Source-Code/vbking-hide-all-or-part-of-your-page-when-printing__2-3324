<div align="center">

## Hide all or part of your page when printing


</div>

### Description

Allows you to hide all or part of your page when it is printed or previewed. This script is very usefull for hiding navigation menus and other controls, for a cleaner printout.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[VBKing](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/vbking.md)
**Level**          |Beginner
**User Rating**    |4.8 (53 globes from 11 users)
**Compatibility**  |
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__2-57.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/vbking-hide-all-or-part-of-your-page-when-printing__2-3324/archive/master.zip)





### Source Code

```
<HTML>
<SCRIPT>
<!--
// Hide tags with id="noprint"
//when printing
function printSetup()
{
var a = document.all.item("noprint");
if (a!=null) {
 if (a.length!=null) {
 //multiple tags found
 for (i=0; i< a.length; i++) {
 a(i).style.display = window.event.type == "beforeprint" ? "none" :"inline";
 }
 } else
 //only one tag
 a.style.display = window.event.type == "beforeprint" ? "none" :"inline";
}
}
//-->
</SCRIPT>
<body onbeforeprint="printSetup()" onafterprint="printSetup()">
<p>You can see me and print me <br>
 <!-- set the tag id to "noprint" for elements you want displayed, but not printed -->
 <h2 id="noprint">You can see me, but not print</h2>
 <SPAN id="noprint">
 <br><hr>Works with SPAN and other tags
 </SPAN>
</BODY>
```

