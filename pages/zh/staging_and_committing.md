---
view: page
title: "七、暂存与提交"
---

<p>git中的暂存步骤可以使你在工作目录中继续进行修改，直到你决定与版本控制进行交互，它允许你把所做的修改记录在小的提交中。</p>

<p>假设你已经修改了三个文件(<code>a. html</code>，<code>b. html</code>以及<code>c. html</code>)。随后由于对<code>c. html</code>的修改在逻辑上与前两个文件并不相关，因此你需要（依次）提交所有的修改，以使得对<code>a. html</code>和<code>b. html</code>的修改作为一个单独的提交，而将对<code>c. html</code>的修改作为另外一个单独的提交。</p>

<p>理论上你可以进行以下操作：</p>

<pre class="instructions">git add a.html
git add b.html
git commit -m "Changes for a and b"</pre>

<pre class="instructions">git add c.html
git commit -m "Unrelated change to c"</pre>

<p>将暂存与提交操作分开，可以使你有机会更加容易地定制哪些（修改）可以被提交。</p>
