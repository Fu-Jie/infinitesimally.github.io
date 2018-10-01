---
# layout    :
title     : vba_sendkeys语句
date      : 2018-10-01 16:13:31
categories: vba
classes   : wide
# permalink : /powershell/
---

## sendkeys 语句

将一个或多个按键消息发送到活动窗口，就如同在键盘上进行输入一样。

<b>语法</b>


<b>sendkeys</b> 语句的语法具有以下几个命名参数：

<table cellpadding=4 cellspacing=4 cols=2>

<tr valign="top">
<th width=12%>部分</th>
<th width=88%>描述</th>
</tr>

<tr valign="top">
<td class=t width=12%><b><i>string</i></b></td>
<td class=t width=88%>必需的。字符串表达式，指定要发送的按键消息。</td>
</tr>

<tr valign="top">
<td class=t width=12%><b><i>wait</i></b></td>
<td class=t width=88%>可选的。指定等待方式的 boolean值。如果为 <b>false</b>（缺省值），则控件在按键发送出去之后立刻返回到过程。如果为 <b>true</b>，则按键消息必须在控件返回到过程之前加以处理。</td>
</tr>
</table><br>



<b>说明</b>
{% raw %}
每个按键由一个或多个字符表示。为了指定单一键盘字符，必须按字符本身的键。例如，为了表示字母 a，可以用 "a" 作为 <b><i>string</i></b>。为了表示多个字符，就必须在字符后面直接加上另一个字符。例如，要表示 a、b 及 c，可用 "abc" 作为 <b><i>string</i></b>。

对 <b>sendkeys</b> 来说，加号 (<b>+</b>)、插入符 (<b>^</b>)、百分比符号 (<b>%</b>)、上划线 (<b>~</b>) 及圆括号 <b>( ) </b>都具有特殊意义。为了指定上述任何一个字符，要将它放在大括号 (`{}`) 当中。例如，要指定正号，可用 `{+}` 表示。方括号 ([ ]) 对 <b>sendkeys </b>来说并不具有特殊意义，但必须将它们放在大括号中。在其它应用程序中，方括号有特殊意义，在出现动态数据交换 (dde)的时候，它可能具有重要意义。为了指定大括号字符，请使用 `{{} 及 {}}'。

为了在按下按键时指定那些不显示的字符，例如 enter 或 tab 以及那些表示动作而非字符的按键，请使用下列代码：
{% endraw %}
<table cellpadding=4 cellspacing=4 cols=2>

<tr valign="top">
<th width=25%>按键</th>
<th width=75%>代码</th>
</tr>

<tr valign="top">
<td class=t width=25%>backspace</td>
<td class=t width=75%>`{backspace}`, `{bs}`, 或 `{bksp}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>break</td>
<td class=t width=75%>`{break}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>caps lock</td>
<td class=t width=75%>`{capslock}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>del or delete</td>
<td class=t width=75%>`{delete}` 或 `{del}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>down arrow</td>
<td class=t width=75%>`{down}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>end</td>
<td class=t width=75%>`{end}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>enter </td>
<td class=t width=75%>`{enter}`或 ~</td>
</tr>

<tr valign="top">
<td class=t width=25%>esc</td>
<td class=t width=75%>`{esc}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>help</td>
<td class=t width=75%>`{help}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>home</td>
<td class=t width=75%>`{home}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>ins or insert</td>
<td class=t width=75%>`{insert}` 或 `{ins}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>left arrow</td>
<td class=t width=75%>`{left}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>num lock</td>
<td class=t width=75%>`{numlock}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>page down</td>
<td class=t width=75%>`{pgdn}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>page up</td>
<td class=t width=75%>`{pgup}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>print screen</td>
<td class=t width=75%>`{prtsc}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>right arrow</td>
<td class=t width=75%>`{right}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>scroll lock</td>
<td class=t width=75%>`{scrolllock}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>tab</td>
<td class=t width=75%>`{tab}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>up arrow</td>
<td class=t width=75%>`{up}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>f1</td>
<td class=t width=75%>`{f1}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>f2</td>
<td class=t width=75%>`{f2}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>f3</td>
<td class=t width=75%>`{f3}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>f4</td>
<td class=t width=75%>`{f4}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>f5</td>
<td class=t width=75%>`{f5}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>f6</td>
<td class=t width=75%>`{f6}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>f7</td>
<td class=t width=75%>`{f7}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>f8</td>
<td class=t width=75%>`{f8}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>f9</td>
<td class=t width=75%>`{f9}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>f10</td>
<td class=t width=75%>`{f10}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>f11</td>
<td class=t width=75%>`{f11}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>f12</td>
<td class=t width=75%>`{f12}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>f13</td>
<td class=t width=75%>`{f13}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>f14</td>
<td class=t width=75%>`{f14}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>f15</td>
<td class=t width=75%>`{f15}`</td>
</tr>

<tr valign="top">
<td class=t width=25%>f16</td>
<td class=t width=75%>`{f16}`</td>
</tr>
</table><br>



为了指定那些与 shift、ctrl 及 alt 等按键结合的组合键，可在这些按键码的前面放置一个或多个代码，这些代码列举如下：

<table cellpadding=4 cellspacing=4 cols=2>

<tr valign="top">
<th width=12%>按键</th>
<th width=88%>代码</th>
</tr>

<tr valign="top">
<td class=t width=12%>shift</td>
<td class=t width=88%>+</td>
</tr>

<tr valign="top">
<td class=t width=12%>ctrl </td>
<td class=t width=88%>^</td>
</tr>

<tr valign="top">
<td class=t width=12%>alt</td>
<td class=t width=88%>%</td>
</tr>
</table><br>



为了说明在按下其它按键时应同时按下 shift、ctrl、及 alt 的任意组合键，请把那些按键的码放在括号当中。例如，为了说明按下 e 与 c 的时候同时按下 shift 键，请使用 "+(ec)"。为了说明在按下 e 的时候同时按下 shift 键，但接着按 c 而不按 shift，则使用 "+ec"。

为了指定重复键，使用 `{key number}` 的形式。必须在 key 与 number 之间放置一个空格。例如，`{left 42}` 意指 42 次按下 left arrow 键；`{h 10}` 则是指 10 次按下 h 键。

 也无法将 print screen 按键 `{prtsc}` 发送到任何应用程序。






















































