---
view: page
title: "一、初始准备"
---

<h3>目标</h3>

<ul><li>为接下来学习Git做好充足的准备。</li></ul>

<h2><em>01</em> 设置用户名与电子邮箱地址</h2>

<p>如果你之前从未使用过git，首先需要设置用户名和电子邮箱地址。执行以下命令可以让git知道你的名字与电子邮箱地址。如果git已经安装好了，则可以直接跳到最后一行。</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git config --global user.name "你的名字"
git config --global user.email "你的邮箱地址@后缀.com"</pre>

<h2><em>02</em> 安装选项 行结束符</h2>

<p>使用Unix/Mac的用户：</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git config --global core.autocrlf input
git config --global core.safecrlf true</pre>

<p>使用Windows的用户：</p>

<h4 class="h4-pre">运行：</h4>

<pre class="instructions">git config --global core.autocrlf true
git config --global core.safecrlf true</pre>
