---
view: page
title: "24. Criando um Branch"
---

<h3>Metas</h3>

<ul><li>Aprender como criar um branch local no repositório</li></ul>

<p>É hora de fazer o nosso hello world ser mais expressivo. Como isso pode demorar um pouco, é melhor mover essas modificações para um novo branch, isolando-as das modificações do branch master.</p>

<h2><em>01</em> Crie um branch</h2>

<p>Vamos nomear o nosso novo branch como "style".</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout -b style
git status</pre>

<p class="note"><strong>Nota: </strong><code>git checkout -b &lt;branch name&gt;</code> é o atalho de <code>git branch &lt;branch name&gt;</code> seguido por <code>git checkout &lt;branch name&gt;</code>.</p>

<p>Note que o comando <code>git status</code> avisa que você está no branch style.</p>

<h2><em>02</em> Adicione o arquivo style.css</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">touch lib/style.css</pre>

<h4 class="h4-pre">Arquivo: <em>lib/style.css</em></h4>

<pre class="file">h1 {
  color: red;
}</pre>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git add lib/style.css
git commit -m "Added css stylesheet"</pre>

<h2><em>03</em> Mude a página principal</h2>

<p>Atualize o arquivo <code>hello.html</code> para usar o style.css.</p>

<h4 class="h4-pre">Arquivo: <em>lib/hello.html</em></h4>

<pre class="file">&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;
&lt;html&gt;
  &lt;head&gt;
<strong>    &lt;link type="text/css" rel="stylesheet" media="all" href="style.css" /&gt;</strong>
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git add lib/hello.html
git commit -m "Hello uses style.css"</pre>

<h2><em>04</em> Mude o index.html</h2>

<p>Atualide o arquivo <code>index.html</code> para que ele use <code>style.css</code></p>

<h4 class="h4-pre">Arquivo: <em>index.html</em></h4>

<pre class="file">&lt;html&gt;
<strong>  &lt;head&gt;
    &lt;link type="text/css" rel="stylesheet" media="all" href="lib/style.css" /&gt;
  &lt;/head&gt;</strong>
  &lt;body&gt;
    &lt;iframe src="lib/hello.html" width="200" height="200" /&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git add index.html
git commit -m "Updated index.html"</pre>

<h2><em>05</em> Próximo</h2>

<p>Agora nós temos um novo branch chamado style com três novos commits. A próxima lição vai te mostrar como navegar e alternar entre branches.</p>
