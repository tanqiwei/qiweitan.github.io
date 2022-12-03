
记录一下关于JDK和JRE的HTML源码。

```html

<?xml version="1.0" encoding="utf-8"?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html lang="en-US" xmlns="http://www.w3.org/1999/xhtml" xml:lang=
"en-US">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<style>
a.ahead {
  FONT-SIZE: 75%;
  COLOR: black;
  FONT-FAMILY: Arial, Helvetica, sans-serif;
  TEXT-DECORATION: none
}

a.ahead:visited {
  FONT-SIZE: 75%; 
  COLOR: black; 
  FONT-FAMILY: Arial, Helvetica, sans-serif; 
  TEXT-DECORATION: none
}

a.atext {
  FONT-SIZE: 100%;
  COLOR: black; 
  FONT-FAMILY: Arial, Helvetica, sans-serif; 
  FONT-WEIGHT: bold; TEXT-DECORATION: none
}

a.atext:visited {
  FONT-SIZE: 100%;
  COLOR: black; 
  FONT-FAMILY: Arial, Helvetica, sans-serif; 
  FONT-WEIGHT: bold; TEXT-DECORATION: none
}

a:hover { 
  TEXT-DECORATION:underline 
}

.table {
  border-collapse: collapse;
  border: 0px;
}

.tablerows {
  width: 100%;
  height: 100%;
  border: 0px;
  border-collapse: separate;
  border-spacing: 0px;
}

.tdbody {
  border-collapse: separate;
  border: 1px solid white;
  PADDING-RIGHT: 0.4em;
  PADDING-LEFT: 0.4em;
  VERTICAL-ALIGN: middle;
  LINE-HEIGHT: 90%;
  HEIGHT: 1.9em;
  TEXT-ALIGN: center;
}

td.tdhead > a, td.tdleftside > a, td.tdrightside > a {
  text-decoration: underline;
}

.tdhead {
  border: 2px solid white;
  PADDING-RIGHT: 0.5em;
  VERTICAL-ALIGN:middle;
  TEXT-ALIGN: right;
/*  
  BORDER-TOP-WIDTH: 0px;
  PADDING-RIGHT: 0.5em;
  BORDER-LEFT-WIDTH: 0px;
  BORDER-BOTTOM-WIDTH: 0px;
  VERTICAL-ALIGN:middle;
  TEXT-ALIGN: right;
  BORDER-RIGHT-WIDTH: 0px
*/
}

.tdleftside {
  border-color: black;
  border-style: solid;
  BORDER-TOP-WIDTH: 2px;
  PADDING-LEFT: 0.25em;
  PADDING-RIGHT: 0.25em;
  BORDER-LEFT-WIDTH: 2px;
  BORDER-BOTTOM-WIDTH: 2px;
  VERTICAL-ALIGN: middle;
  TEXT-ALIGN: left;
  BORDER-RIGHT: 0px solid white;
}

.tdrightside {
  border-left: 0px;
  border-right: 2px solid black;
  border-top: 2px solid black;
  border-bottom: 2px solid black;
  PADDING-RIGHT: 0.25em;
  PADDING-LEFT: 0.25em;
  VERTICAL-ALIGN: middle;
  TEXT-ALIGN: center
}

/***********************************************/
/* Layout div styles                           */
/***********************************************/

#pageNav{
        float: left;
        /* clear: both; */
        width:178px;
        padding: 0px;
        background-color: #F5f7f7;
        border-right: 1px solid #cccccc;
        border-bottom: 1px solid #cccccc;
        font: small Verdana,sans-serif;
}

#feature{
        float: left;
        /* clear: both; */
}

#content{
        padding: 0px 10px 0px 0px;
        margin:0px 0px 0px 178px;
        border-left: 1px solid #ccd2d2;
}

/***********************************************/
/* HTML tag styles                             */
/***********************************************/

body {
        font-family: Arial,sans-serif;
        color: #333333;
        line-height: 1.166;
        margin: 0px;
        padding: 0px;

}

/******* hyperlink and anchor tag styles *******/

a:hover {
        text-decoration: underline;
}

/************** header tag styles **************/

h1 {
  text-align: center;
}

h2 {
 font: bold 100% Arial,sans-serif;
 color: #333333;
 margin: 0px;
 padding: 0px;
}

h3 {
 font: bold 100% Arial,sans-serif;
 color: #334d55;
 margin: 0px;
 padding: 0px;
}

h4 {
 font: 100% Arial,sans-serif;
 color: #333333;
 margin: 0px;
 padding: 0px;
}

h5 {
 font: 100% Arial,sans-serif;
 color: #334d55;
 margin: 0px;
 padding: 0px;
}

/************** feature styles *****************/

.feature {
        padding: 0px 0px 10px 10px;
        font-size: 100%;
        min-height: 200px;
        height: 200px;
}
html>body .feature {height: auto;}

.feature h3 {
        font: bold 175% Arial,sans-serif;
        color: #000000;
        padding: 30px 0px 5px 0px;
}

.feature img {
        float: left;
        padding: 0px 10px 0px 0px;
}


/*************** story styles ******************/

.story {
        padding: 10px 0px 0px 10px;
        font-size: 100%;
}

.story h3{
        font: bold 125% Arial,sans-serif;
        color: #000000;
}

.story p {
        padding: 0px 0px 10px 0px;
}

.story a {
        font:  Arial,sans-serif;
}

.story a:hover {
                text-decoration: underline;
}

.story a.capsule{
        font: bold 1em Arial,sans-serif;
        color: #005FA9;
        display:block;
        padding-bottom: 5px;
}

.story a.capsule:hover{
        text-decoration: underline;
}

.story a.notHref {
        text-decoration: none;
}

td.storyLeft{
        padding-right: 12px;
}

.storyLeft a {
        font: bold 100% Arial,sans-serif;
}

/************* relatedLinks styles **************/

/*

.relatedLinks{
        margin: 0px;
        padding: 0px 0px 10px 10px;
        border-bottom: 1px solid #cccccc;
        font: 90% Verdana,sans-serif;

}

.relatedLinks a{
        display: block;
        text-decoration: none;
}

.relatedLinksHeader {
        padding: 10px 0px 2px 0px; 
        font: bold 100% Arial,sans-serif;
}

*/

.relatedLinks {
  margin: 0px;
  padding: 0px 0px 10px 10px;
  border-bottom: 1px solid #cccccc;
  font: 90% Verdana,sans-serif;
}

.relatedLinks ul {
  margin: 0px 0px 0px 17px;
  padding: 0px 0px 0px 0px;
  list-style-position: outside;
  list-style-type:dot;
} 

.relatedLinksHeader {
  padding: 10px 0px 2px 0px; 
  font: bold 100% Arial,sans-serif;
}
</style>




</div>


<table summary="" class="table" cellspacing="0" cellpadding="0">
<!-- Row 1 of 9 -->
<tr valign="top">
<td class="tdleftside" rowspan="9">JDK</td>
<td rowspan="2">&nbsp;</td>
<td class="tdhead" title="Java programming language"><b>Java
Language</b></td>
<!-- Java Language -->
<td>
<table class="tablerows" summary="">
<tr>
<td class="tdbody" bgcolor="#BDBEC0">Java
Language</td>
</tr>
</table>
</td>
<td rowspan="5">&nbsp;</td>
<td rowspan="4">&nbsp;</td>
</tr>
<!-- Row 2 of 9 -->
<tr valign="top">
<td class="tdhead" title="Tools and Tool APIs"><b>Tools &amp;<br />
Tool APIs</b></td>
<td>
<table class="tablerows" summary="">
<tr>
<td class="tdbody" bgcolor="#A3B8CB" title="Java runtime launcher">java</td>
<td class="tdbody" bgcolor="#A3B8CB" title="Java compiler">javac</td>
<td class="tdbody" bgcolor="#A3B8CB" title=
"Java documentation generator">javadoc</td>
<td class="tdbody" bgcolor="#A3B8CB" title="Java archive tool">
jar</td>
<td class="tdbody" bgcolor="#A3B8CB" title=
"Java class file disassembler">javap</td>
<td class="tdbody" bgcolor="#A3B8CB" title=
"Java class dependency analyzer">jdeps</td>
<td class="tdbody" bgcolor="#A3B8CB" title="Scripting tools">
Scripting</td>
</tr>
<tr>
<td class="tdbody" bgcolor="#A3B8CB" title="Security tools">
Security</td>
<td class="tdbody" bgcolor="#A3B8CB" title=
"Monitoring and Management tools">Monitoring</td>
<td class="tdbody" bgcolor="#A3B8CB" title="jconsole">JConsole</td>
<td class="tdbody" bgcolor="#A3B8CB" title="Java VisualVM">VisualVM</td>
<td class="tdbody" bgcolor="#A3B8CB" title="Java Mission Control">JMC</td>
<td class="tdbody" bgcolor="#A3B8CB" title="Java Flight Recorder" colspan="2">JFR</td>
</tr>
<tr>
<td class="tdbody" bgcolor="#A3B8CB" title=
"Java Platform Debugger Architecture">JPDA</td>
<td class="tdbody" bgcolor="#A3B8CB" title=
"Java Virtual Machine Tool Interface">JVM TI</td>
<td class="tdbody" bgcolor="#A3B8CB" title=
"Interface Definition Language and RMI-IIOP tools">IDL</td>
<td class="tdbody" bgcolor="#A3B8CB" title=
"Remote Method Invocation tools">RMI</td>
<td class="tdbody" bgcolor="#A3B8CB" title="Java DB">Java
DB</td>
<td class="tdbody" bgcolor="#A3B8CB" title=
"Deployment, Plug-in and Web Start tools" colspan="2">Deployment</td>
</tr>
<tr>
<td class="tdbody" colspan="2" bgcolor="#A3B8CB" title=
"Internationalization tools">Internationalization</td>
<td class="tdbody" colspan="2" bgcolor="#A3B8CB" title=
"Java Web Services Tools">Web
Services</td>
<td class="tdbody" colspan="3" bgcolor="#A3B8CB" title=
"Troubleshooting tools">Troubleshooting</td>
</tr>
</table>
</td>
</tr>
<!-- Row 3 of 9 -->
<tr valign="top">
<td rowspan="7" class="tdleftside" title=
"Java Runtime Environment">JRE</td>
<td class="tdhead" title="Deployment Technologies"><b>Deployment</b></td>
<td>
<table class="tablerows" summary="">
<tr>
<td class="tdbody" bgcolor="#ED9B4F" title="Java Web Start">
Java Web
Start</td>
<td class="tdbody" bgcolor="#ED9B4F" title=
"Java Plug-In for browsers">Applet / Java Plug-in</td>
</tr>
</table>
</td>
</tr>
<!-- Row 4 of 9 -->
<tr valign="top">
<td class="tdhead" rowspan="2" title="User Interface programming">
<b>User Interface<br />
Toolkits</b></td>
<td>
<table class="tablerows" summary="">
<tr>
<td class="tdbody" bgcolor="#E76F00" title="JavaFX">JavaFX</td>
</tr>
</table>
</td>
</tr>
<!-- Row 5 of 9 -->
<tr valign="top">
<td>
<table class="tablerows" summary="">
<tr>
<td class="tdbody" bgcolor="#E76F00" title=
"Graphical user interface components">Swing</td>
<td class="tdbody" bgcolor="#E76F00" title=
"2D graphics, text and images">Java 2D</td>
<td class="tdbody" bgcolor="#E76F00" title=
"Abstract Window Toolkit">AWT</td>
<td class="tdbody" colspan="2" bgcolor="#E76F00" title=
"Assistive technologies for user interfaces">Accessibility</td>
</tr>
<tr>
<td class="tdbody" bgcolor="#E76F00" title=
"Drag and drop data transfer">Drag and
Drop</td>
<td class="tdbody" bgcolor="#E76F00" title=
"Input Method Framework">Input Methods</td>
<td class="tdbody" bgcolor="#E76F00" title=
"Image input/output API">Image
I/O</td>
<td class="tdbody" bgcolor="#E76F00" title="Print service API">
Print
Service</td>
<td class="tdbody" bgcolor="#E76F00" title="MIDI API">Sound</td>
</tr>
</table>
</td>
<td class="tdrightside" rowspan="4" title=
"Java SE API. See API Documentation section for more links.">
Java SE<br />
API</td>
</tr>
<!-- Row 6 of 9 -->
<tr valign="top">
<td class="tdhead" title="Integration libraries"><b>Integration<br />
Libraries</b></td>
<td>
<table class="tablerows" summary="">
<tr>
<td class="tdbody" bgcolor="#B2BC00" title=
"CORBA Interface Definition Language API">IDL</td>
<td class="tdbody" bgcolor="#B2BC00" title=
"Java Database Connectivity API">JDBC</td>
<td class="tdbody" bgcolor="#B2BC00" title=
"Java Naming and Directory Interface API">JNDI</td>
<td class="tdbody" bgcolor="#B2BC00" title=
"Remote Method Invocation API">RMI</td>
<td class="tdbody" bgcolor="#B2BC00" title=
"RMI interfaces over IIOP">RMI-IIOP</td>
<td class="tdbody" bgcolor="#B2BC00" title=
"Scripting for the Java Platform">Scripting</td>
</tr>
</table>
</td>
<td class="tdrightside" rowspan="3" title=
"Compact Profiles">
Compact<br/> Profiles</td>
</tr>
<!-- Row 7 of 9 -->
<tr valign="top">
<td class="tdhead" title=
"Base libraries other than java.lang and java.util"><b>Other
Base<br />
Libraries</b></td>
<td>
<table class="tablerows" summary="">
<tr>
<td class="tdbody" bgcolor="#C69200" title=
"Java Beans component API">Beans</td>
<td class="tdbody" bgcolor="#C69200" title="Security API">Security</td>
<td class="tdbody" bgcolor="#C69200" title="Object Serialization">
Serialization</td>
<td class="tdbody" bgcolor="#C69200" title=
"Package extension mechanism">Extension
Mechanism</td>
</tr>
<tr>
<td class="tdbody" bgcolor="#C69200" title=
"Java Management Extensions">JMX</td>
<td class="tdbody" bgcolor="#C69200" nowrap="nowrap" title=
"Java API for XML Processing">XML JAXP</td>
<td class="tdbody" bgcolor="#C69200" title="Networking API">
Networking</td>
<td class="tdbody" bgcolor="#C69200" title=
"Endorsed Standards Override Mechanism">Override
Mechanism</td>
</tr>
<tr>
<td class="tdbody" bgcolor="#C69200" title="Java Native Interface">
JNI</td>
<td class="tdbody" bgcolor="#C69200" title="Date and Time">Date and
Time</td>
<td class="tdbody" bgcolor="#C69200" title="Input/Output API">
Input/Output</td>
<td class="tdbody" bgcolor="#C69200" title=
"Internationalization of applications">Internationalization</td>
</tr>
</table>
</td>
</tr>
<!-- Row 8 of 9 -->
<tr valign="top">
<td class="tdhead" title="java.lang and java.util libraries">
<b>lang and util<br />
Base Libraries</b></td>
<td>
<table class="tablerows" summary="">
<tr>
<td class="tdbody" colspan="5" bgcolor="#FFC726" title=
"java.lang and java.util packages">lang and
util</td>
</tr>
<tr>
<td class="tdbody" bgcolor="#FFC726" title="Math classes">Math</td>
<td class="tdbody" bgcolor="#FFC726" title="Collections framework">
Collections</td>
<td class="tdbody" bgcolor="#FFC726" title="Reference Objects API">
Ref
Objects</td>
<td class="tdbody" colspan="2" bgcolor="#FFC726" title=
"Regular expressions">Regular
Expressions</td>
</tr>
<tr>
<td class="tdbody" bgcolor="#FFC726" title="Logging API">Logging</td>
<td class="tdbody" bgcolor="#FFC726" title=
"JVM Monitoring and Management">Management</td>
<td class="tdbody" bgcolor="#FFC726" title="Instrumentation">
Instrumentation</td>
<td class="tdbody" colspan="2" bgcolor="#FFC726" title=
"Concurrency utilities">Concurrency
Utilities</td>
</tr>
<tr>
<td class="tdbody" bgcolor="#FFC726" title="Reflection API">
Reflection</td>
<td class="tdbody" bgcolor="#FFC726" title=
"Package version identification">Versioning</td>
<td class="tdbody" bgcolor="#FFC726" title="Preferences API">
Preferences API</td>
<td class="tdbody" bgcolor="#FFC726" title=
"Java archive file format">JAR</td>
<td class="tdbody" bgcolor="#FFC726" title=
"Zip and gzip file formats">Zip</td>
</tr>
</table>
</td>
</tr>
<!-- Row 9 of 9 -->
<tr valign="top">
<td class="tdhead" title="Java Virtual Machine"><b>Java Virtual
Machine</b></td>
<td>
<table class="tablerows" summary="">
<tr>
<td class="tdbody" bgcolor="#C5D5A9">Java HotSpot Client
and Server VM</td>
</tr>
</table>
</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
</table>
<!-- ################################### -->
<!-- END OF TABLE -->
<!-- ################################### -->

<!-- Extra <br/> so that link in the left panel that extend below the layer cake work -->

</div>
<!-- id="content" -->
<!-- commenting out JDK 7-specific links; will replace with corresponding JDK 8 links as we get closer
<div class="story">
<h2><a name="NewFeature" id="NewFeature" class="notHref"></a>What's
New in Documentation</h2>
<p>This section will contain information about new features in the
Java platform.</p>
</div>
-->
<!-- class="feature" --></div>

</body>
</html>
```
