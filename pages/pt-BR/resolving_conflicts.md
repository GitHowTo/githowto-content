---
view: page
title: "30. Resolvendo conflitos"
---

<h3>Metas</h3>

<ul><li>Aprender a resolver conflitos de merge</li></ul>

<h2><em>01</em> Fazer merge do branch master com o style</h2>

<p>Vamos voltar para o branch style e fazer um merge dele com um novo master.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout style
git merge master</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git checkout style
Switched to branch 'style'
$ git merge master
Auto-merging lib/hello.html
CONFLICT (content): Merge conflict in lib/hello.html
Automatic merge failed; fix conflicts and then commit the result.</pre>

<p>Se voc&ecirc; abrir o <code>lib/hello.html</code> voc&ecirc; ver&aacute;:</p>

<h4 class="h4-pre">Arquivo: <em>lib/hello.html</em></h4>

<pre class="file">&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;
&lt;html&gt;
  &lt;head&gt;
&lt;&lt;&lt;&lt;&lt;&lt;&lt; HEAD
    &lt;link type="text/css" rel="stylesheet" media="all" href="style.css" /&gt;
=======
    &lt;!-- no style --&gt;
&gt;&gt;&gt;&gt;&gt;&gt;&gt; master
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello,World! Life is great!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;
</pre>

<p>A primeira se&ccedil;&atilde;o e a vers&atilde;o do branch atual (style) head. A segunda se&ccedil;&atilde;o &eacute; a vers&atilde;o do branch master.</p>

<h2><em>02</em> Resolu&ccedil;&atilde;o do conflito</h2>

<p>Voc&ecirc; precisa resolver o conflito manualmente. Fa&ccedil;a mudan&ccedil;as no <code>lib/hello.html</code> para alcan&ccedil;ar o seguinte resultado.</p>

<h4 class="h4-pre">Arquivo: <em>lib/hello.html</em></h4>

<pre class="file">&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;link type="text/css" rel="stylesheet" media="all" href="style.css" /&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World! Life is great!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h2><em>03</em> Fa&ccedil;a o commit de uma resolu&ccedil;&atilde;o de conflito</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git add lib/hello.html
git commit -m "Merged master fixed conflict."</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git add lib/hello.html
$ git commit -m "Merged master fixed conflict."
Recorded resolution for 'lib/hello.html'.
[style 645c4e6] Merged master fixed conflict.</pre>

<h2><em>04</em> Merging avan&ccedil;ado</h2>

<p>Git n&atilde;o tem ferramentas gr&aacute;ficas de merging, mas aceita qualquer ferramenta de merge produzida por terceiros. (<a href="http://stackoverflow.com/questions/137102/whats-the-best-visual-merge-tool-for-git">leia mais sobre essas ferramentas no StackOverflow</a>.)</p>
