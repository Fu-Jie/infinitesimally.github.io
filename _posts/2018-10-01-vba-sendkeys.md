---
layout    : none
title     : vba_sendkeys语句
date      : 2018-10-01 16:13:31
categories: vba
classes   : wide
# permalink : /powershell/
---








<div style="display:none;">
<mshelp:link id=hhobj_4 keywords="defnamedarguments" indexmoniker="!defaultassociativeindex" errorurl="" disambiguator="menu"  tabindex=0></mshelp:link>

<mshelp:link id=hhobj_5 keywords="defstringexpression" indexmoniker="!defaultassociativeindex" errorurl="" disambiguator="menu"  tabindex=0></mshelp:link>

<mshelp:link id=hhobj_6 keywords="defprocedure" indexmoniker="!defaultassociativeindex" errorurl="" disambiguator="menu"  tabindex=0></mshelp:link>

<mshelp:link id=hhobj_7 keywords="defdde" indexmoniker="!defaultassociativeindex" errorurl="" disambiguator="menu"  tabindex=0></mshelp:link>

</div>



<h1><a name="vastmsendkeys"></a>sendkeys 语句</h1>

<p class=t>将一个或多个按键消息发送到活动窗口，就如同在键盘上进行输入一样。</p>

<p><b>语法</b></p>

<p class=syn><b>sendkeys</b> <b><i>string</i></b>[, <b><i>wait</i></b>]</p>

<p class=t><b>sendkeys</b> 语句的语法具有以下几个<a href="javascript:hhobj_4.click()">命名参数</a>：</p>

<table cellpadding=4 cellspacing=4 cols=2>

<tr valign="top">
<th width=12%>部分</th>
<th width=88%>描述</th>
</tr>

<tr valign="top">
<td class=t width=12%><b><i>string</i></b></td>
<td class=t width=88%>必需的。<a href="javascript:hhobj_5.click()">字符串表达式</a>，指定要发送的按键消息。</td>
</tr>

<tr valign="top">
<td class=t width=12%><b><i>wait</i></b></td>
<td class=t width=88%>可选的。指定等待方式的 booleandefbooleandatatype@veendf98.chm 值。如果为 <b>false</b>（缺省值），则控件在按键发送出去之后立刻返回到<a href="javascript:hhobj_6.click()">过程</a>。如果为 <b>true</b>，则按键消息必须在控件返回到过程之前加以处理。</td>
</tr>
</table><br>

<p></p>

<p><b>说明</b></p>

<p class=t>每个按键由一个或多个字符表示。为了指定单一键盘字符，必须按字符本身的键。例如，为了表示字母 a，可以用 <code>"a"</code> 作为 <b><i>string</i></b>。为了表示多个字符，就必须在字符后面直接加上另一个字符。例如，要表示 a、b 及 c，可用 <code>"abc"</code> 作为 <b><i>string</i></b>。</p>

<p class=t>对 <b>sendkeys</b> 来说，加号 (<b>+</b>)、插入符 (<b>^</b>)、百分比符号 (<b>%</b>)、上划线 (<b>~</b>) 及圆括号 <b>( ) </b>都具有特殊意义。为了指定上述任何一个字符，要将它放在大括号 ({}) 当中。例如，要指定正号，可用 {<code>+}</code> 表示。方括号 ([ ]) 对 <b>sendkeys </b>来说并不具有特殊意义，但必须将它们放在大括号中。在其它应用程序中，方括号有特殊意义，在出现<a href="javascript:hhobj_7.click()">动态数据交换 (dde)</a> 的时候，它可能具有重要意义。为了指定大括号字符，请使用 {{}<code> </code>及 {}}。</p>

<p class=t>为了在按下按键时指定那些不显示的字符，例如 enter 或 tab 以及那些表示动作而非字符的按键，请使用下列代码：</p>

<table cellpadding=4 cellspacing=4 cols=2>

<tr valign="top">
<th width=25%>按键</th>
<th width=75%>代码</th>
</tr>

<tr valign="top">
<td class=t width=25%>backspace</td>
<td class=t width=75%>{<code>backspace}</code>, {<code>bs}</code>, 或 {<code>bksp}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>break</td>
<td class=t width=75%>{<code>break}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>caps lock</td>
<td class=t width=75%>{<code>capslock}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>del or delete</td>
<td class=t width=75%>{<code>delete}</code> 或 {<code>del}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>down arrow</td>
<td class=t width=75%>{<code>down}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>end</td>
<td class=t width=75%>{<code>end}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>enter </td>
<td class=t width=75%>{<code>enter}</code>或 <code>~</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>esc</td>
<td class=t width=75%>{<code>esc}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>help</td>
<td class=t width=75%>{<code>help}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>home</td>
<td class=t width=75%>{<code>home}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>ins or insert</td>
<td class=t width=75%>{<code>insert}</code> 或 {<code>ins}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>left arrow</td>
<td class=t width=75%>{<code>left}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>num lock</td>
<td class=t width=75%>{<code>numlock}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>page down</td>
<td class=t width=75%>{<code>pgdn}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>page up</td>
<td class=t width=75%>{<code>pgup}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>print screen</td>
<td class=t width=75%>{<code>prtsc}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>right arrow</td>
<td class=t width=75%>{<code>right}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>scroll lock</td>
<td class=t width=75%>{<code>scrolllock}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>tab</td>
<td class=t width=75%>{<code>tab}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>up arrow</td>
<td class=t width=75%>{<code>up}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>f1</td>
<td class=t width=75%>{<code>f1}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>f2</td>
<td class=t width=75%>{<code>f2}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>f3</td>
<td class=t width=75%>{<code>f3}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>f4</td>
<td class=t width=75%>{<code>f4}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>f5</td>
<td class=t width=75%>{<code>f5}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>f6</td>
<td class=t width=75%>{<code>f6}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>f7</td>
<td class=t width=75%>{<code>f7}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>f8</td>
<td class=t width=75%>{<code>f8}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>f9</td>
<td class=t width=75%>{<code>f9}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>f10</td>
<td class=t width=75%>{<code>f10}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>f11</td>
<td class=t width=75%>{<code>f11}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>f12</td>
<td class=t width=75%>{<code>f12}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>f13</td>
<td class=t width=75%>{<code>f13}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>f14</td>
<td class=t width=75%>{<code>f14}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>f15</td>
<td class=t width=75%>{<code>f15}</code></td>
</tr>

<tr valign="top">
<td class=t width=25%>f16</td>
<td class=t width=75%>{<code>f16}</code></td>
</tr>
</table><br>

<p></p>

<p class=t>为了指定那些与 shift、ctrl 及 alt 等按键结合的组合键，可在这些按键码的前面放置一个或多个代码，这些代码列举如下：</p>

<table cellpadding=4 cellspacing=4 cols=2>

<tr valign="top">
<th width=12%>按键</th>
<th width=88%>代码</th>
</tr>

<tr valign="top">
<td class=t width=12%>shift</td>
<td class=t width=88%><code>+</code></td>
</tr>

<tr valign="top">
<td class=t width=12%>ctrl </td>
<td class=t width=88%><code>^</code></td>
</tr>

<tr valign="top">
<td class=t width=12%>alt</td>
<td class=t width=88%><code>%</code></td>
</tr>
</table><br>

<p></p>

<p class=t>为了说明在按下其它按键时应同时按下 shift、ctrl、及 alt 的任意组合键，请把那些按键的码放在括号当中。例如，为了说明按下 e 与 c 的时候同时按下 shift 键，请使用 "<code>+(ec)</code>"。为了说明在按下 e 的时候同时按下 shift 键，但接着按 c 而不按 shift，则使用 "<code>+ec</code>"。</p>

<p class=t>为了指定重复键，使用 {<code>key number} </code>的形式。必须在 <code>key</code> 与 <code>number</code> 之间放置一个空格。例如，{<code>left 42}</code> 意指 42 次按下 left arrow 键；{<code>h 10}</code> 则是指 10 次按下 h 键。</p>

<p class=nt><b>注意</b>   不能用 <b>sendkeys </b>将按键消息发送到这样一个应用程序，这个应用程序并没有被设计成在 microsoft windows  or macintosh中运行。<b>sendkeys</b> 也无法将 print screen 按键 {<code>prtsc</code>} 发送到任何应用程序。</p>

<p class=nt></p>

<p class=t></p>

<p class=t></p>

<p class=t></p>

<p class=t></p>

<p class=t></p>










































