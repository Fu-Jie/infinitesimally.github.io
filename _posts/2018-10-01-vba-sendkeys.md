---
# layout    : archive
title     : VBA_Sendkeys语句
date      : 2018-10-01 16:13:31
categories: VBA
classes   : wide
# permalink : /PowerShell/
---




<DIV STYLE="display:none;">
<MSHelp:link id=hhobj_4 keywords="defnamedarguments" indexMoniker="!DefaultAssociativeIndex" errorURL="" disambiguator="menu"  TABINDEX=0></MSHelp:link>

<MSHelp:link id=hhobj_5 keywords="defstringexpression" indexMoniker="!DefaultAssociativeIndex" errorURL="" disambiguator="menu"  TABINDEX=0></MSHelp:link>

<MSHelp:link id=hhobj_6 keywords="defprocedure" indexMoniker="!DefaultAssociativeIndex" errorURL="" disambiguator="menu"  TABINDEX=0></MSHelp:link>

<MSHelp:link id=hhobj_7 keywords="defdde" indexMoniker="!DefaultAssociativeIndex" errorURL="" disambiguator="menu"  TABINDEX=0></MSHelp:link>

</DIV>



<H1><A NAME="vastmsendkeys"></A>SendKeys 语句</H1>



<P class=T>将一个或多个按键消息发送到活动窗口，就如同在键盘上进行输入一样。</P>

<p><B>语法</B></p>

<P class=SYN><B>SendKeys</B> <B><I>string</I></B>[, <B><I>wait</I></B>]</P>

<P class=T><B>SendKeys</B> 语句的语法具有以下几个<A HREF="JavaScript:hhobj_4.Click()">命名参数</A>：</P>

<TABLE cellpadding=4 cellspacing=4 cols=2>

<TR VALIGN="top">
<TH width=12%>部分</TH>
<TH width=88%>描述</TH>
</TR>

<TR VALIGN="top">
<TD class=T width=12%><B><I>string</I></B></TD>
<TD class=T width=88%>必需的。<A HREF="JavaScript:hhobj_5.Click()">字符串表达式</A>，指定要发送的按键消息。</TD>
</TR>

<TR VALIGN="top">
<TD class=T width=12%><B><I>Wait</I></B></TD>
<TD class=T width=88%>可选的。指定等待方式的 BooleandefBooleanDataType@veendf98.chm 值。如果为 <B>False</B>（缺省值），则控件在按键发送出去之后立刻返回到<A HREF="JavaScript:hhobj_6.Click()">过程</A>。如果为 <B>True</B>，则按键消息必须在控件返回到过程之前加以处理。</TD>
</TR>
</TABLE><BR>

<p></P>

<p><B>说明</B></p>

<P class=T>每个按键由一个或多个字符表示。为了指定单一键盘字符，必须按字符本身的键。例如，为了表示字母 A，可以用 <CODE>"A"</CODE> 作为 <B><I>string</I></B>。为了表示多个字符，就必须在字符后面直接加上另一个字符。例如，要表示 A、B 及 C，可用 <CODE>"ABC"</CODE> 作为 <B><I>string</I></B>。</P>

<P class=T>对 <B>SendKeys</B> 来说，加号 (<B>+</B>)、插入符 (<B>^</B>)、百分比符号 (<B>%</B>)、上划线 (<B>~</B>) 及圆括号 <B>( ) </B>都具有特殊意义。为了指定上述任何一个字符，要将它放在大括号 ({}) 当中。例如，要指定正号，可用 {<CODE>+}</CODE> 表示。方括号 ([ ]) 对 <B>SendKeys </B>来说并不具有特殊意义，但必须将它们放在大括号中。在其它应用程序中，方括号有特殊意义，在出现<A HREF="JavaScript:hhobj_7.Click()">动态数据交换 (DDE)</A> 的时候，它可能具有重要意义。为了指定大括号字符，请使用 {{}<CODE> </CODE>及 {}}。</P>

<P class=T>为了在按下按键时指定那些不显示的字符，例如 ENTER 或 TAB 以及那些表示动作而非字符的按键，请使用下列代码：</P>

<TABLE cellpadding=4 cellspacing=4 cols=2>

<TR VALIGN="top">
<TH width=25%>按键</TH>
<TH width=75%>代码</TH>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>BACKSPACE</TD>
<TD class=T width=75%>{<CODE>BACKSPACE}</CODE>, {<CODE>BS}</CODE>, 或 {<CODE>BKSP}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>BREAK</TD>
<TD class=T width=75%>{<CODE>BREAK}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>CAPS LOCK</TD>
<TD class=T width=75%>{<CODE>CAPSLOCK}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>DEL or DELETE</TD>
<TD class=T width=75%>{<CODE>DELETE}</CODE> 或 {<CODE>DEL}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>DOWN ARROW</TD>
<TD class=T width=75%>{<CODE>DOWN}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>END</TD>
<TD class=T width=75%>{<CODE>END}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>ENTER </TD>
<TD class=T width=75%>{<CODE>ENTER}</CODE>或 <CODE>~</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>ESC</TD>
<TD class=T width=75%>{<CODE>ESC}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>HELP</TD>
<TD class=T width=75%>{<CODE>HELP}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>HOME</TD>
<TD class=T width=75%>{<CODE>HOME}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>INS or INSERT</TD>
<TD class=T width=75%>{<CODE>INSERT}</CODE> 或 {<CODE>INS}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>LEFT ARROW</TD>
<TD class=T width=75%>{<CODE>LEFT}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>NUM LOCK</TD>
<TD class=T width=75%>{<CODE>NUMLOCK}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>PAGE DOWN</TD>
<TD class=T width=75%>{<CODE>PGDN}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>PAGE UP</TD>
<TD class=T width=75%>{<CODE>PGUP}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>PRINT SCREEN</TD>
<TD class=T width=75%>{<CODE>PRTSC}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>RIGHT ARROW</TD>
<TD class=T width=75%>{<CODE>RIGHT}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>SCROLL LOCK</TD>
<TD class=T width=75%>{<CODE>SCROLLLOCK}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>TAB</TD>
<TD class=T width=75%>{<CODE>TAB}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>UP ARROW</TD>
<TD class=T width=75%>{<CODE>UP}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>F1</TD>
<TD class=T width=75%>{<CODE>F1}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>F2</TD>
<TD class=T width=75%>{<CODE>F2}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>F3</TD>
<TD class=T width=75%>{<CODE>F3}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>F4</TD>
<TD class=T width=75%>{<CODE>F4}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>F5</TD>
<TD class=T width=75%>{<CODE>F5}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>F6</TD>
<TD class=T width=75%>{<CODE>F6}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>F7</TD>
<TD class=T width=75%>{<CODE>F7}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>F8</TD>
<TD class=T width=75%>{<CODE>F8}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>F9</TD>
<TD class=T width=75%>{<CODE>F9}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>F10</TD>
<TD class=T width=75%>{<CODE>F10}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>F11</TD>
<TD class=T width=75%>{<CODE>F11}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>F12</TD>
<TD class=T width=75%>{<CODE>F12}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>F13</TD>
<TD class=T width=75%>{<CODE>F13}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>F14</TD>
<TD class=T width=75%>{<CODE>F14}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>F15</TD>
<TD class=T width=75%>{<CODE>F15}</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=25%>F16</TD>
<TD class=T width=75%>{<CODE>F16}</CODE></TD>
</TR>
</TABLE><BR>

<p></P>

<P class=T>为了指定那些与 SHIFT、CTRL 及 ALT 等按键结合的组合键，可在这些按键码的前面放置一个或多个代码，这些代码列举如下：</P>

<TABLE cellpadding=4 cellspacing=4 cols=2>

<TR VALIGN="top">
<TH width=12%>按键</TH>
<TH width=88%>代码</TH>
</TR>

<TR VALIGN="top">
<TD class=T width=12%>SHIFT</TD>
<TD class=T width=88%><CODE>+</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=12%>CTRL </TD>
<TD class=T width=88%><CODE>^</CODE></TD>
</TR>

<TR VALIGN="top">
<TD class=T width=12%>ALT</TD>
<TD class=T width=88%><CODE>%</CODE></TD>
</TR>
</TABLE><BR>

<p></P>

<P class=T>为了说明在按下其它按键时应同时按下 SHIFT、CTRL、及 ALT 的任意组合键，请把那些按键的码放在括号当中。例如，为了说明按下 E 与 C 的时候同时按下 SHIFT 键，请使用 "<CODE>+(EC)</CODE>"。为了说明在按下 E 的时候同时按下 SHIFT 键，但接着按 C 而不按 SHIFT，则使用 "<CODE>+EC</CODE>"。</P>

<P class=T>为了指定重复键，使用 {<CODE>key number} </CODE>的形式。必须在 <CODE>key</CODE> 与 <CODE>number</CODE> 之间放置一个空格。例如，{<CODE>LEFT 42}</CODE> 意指 42 次按下 LEFT ARROW 键；{<CODE>h 10}</CODE> 则是指 10 次按下 H 键。</P>

<P class=NT><B>注意</B>   不能用 <B>SendKeys </B>将按键消息发送到这样一个应用程序，这个应用程序并没有被设计成在 Microsoft Windows  or Macintosh中运行。<B>Sendkeys</B> 也无法将 PRINT SCREEN 按键 {<CODE>PRTSC</CODE>} 发送到任何应用程序。</P>

<P class=NT></P>

<P class=T></P>

<P class=T></P>

<P class=T></P>

<P class=T></P>

<P class=T></P>




















