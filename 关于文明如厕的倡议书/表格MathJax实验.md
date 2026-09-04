# Markdown 表格内 MathJax 解析实验

目标：只判断“表格形态”和 MathJax 是否能共存。每组都同时测试红、蓝两个已在普通 Markdown 区域验证成功的命名色。

## A. 纯 Markdown 表格

| 序号 | 内容 |
| :---: | --- |
| 1 | 普通文字基线 |
| 2 | 在坑中小便时，$\color{red}{\textsf{尽量往后站}}$，不要把尿溅到挡板上。 |
| 3 | $\color{blue}{\textsf{蓝色文字也应当正常渲染}}$ |

## B. HTML 表格，但在单元格中用空行切断 raw HTML block

<table>
<tr>
<td width="42" align="center">1</td>
<td>

普通文字基线

</td>
</tr>
<tr>
<td align="center">2</td>
<td>

在坑中小便时，$\color{red}{\textsf{尽量往后站}}$，不要把尿溅到挡板上。

</td>
</tr>
<tr>
<td align="center">3</td>
<td>

$\color{blue}{\textsf{蓝色文字也应当正常渲染}}$

</td>
</tr>
</table>

## C. HTML 表格 + markdown="1"

<table markdown="1">
<tr markdown="1">
<td width="42" align="center" markdown="1">1</td>
<td markdown="1">普通文字基线</td>
</tr>
<tr markdown="1">
<td align="center" markdown="1">2</td>
<td markdown="1">在坑中小便时，$\color{red}{\textsf{尽量往后站}}$，不要把尿溅到挡板上。</td>
</tr>
<tr markdown="1">
<td align="center" markdown="1">3</td>
<td markdown="1">$\color{blue}{\textsf{蓝色文字也应当正常渲染}}$</td>
</tr>
</table>

## D. 原始 HTML 表格对照组

<table>
<tr>
<td width="42" align="center">1</td>
<td>普通文字基线</td>
</tr>
<tr>
<td align="center">2</td>
<td>在坑中小便时，$\color{red}{\textsf{尽量往后站}}$，不要把尿溅到挡板上。</td>
</tr>
<tr>
<td align="center">3</td>
<td>$\color{blue}{\textsf{蓝色文字也应当正常渲染}}$</td>
</tr>
</table>

## E. 表格外基线

红：$\color{red}{\textsf{尽量往后站}}$

蓝：$\color{blue}{\textsf{蓝色文字也应当正常渲染}}$
