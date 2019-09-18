---
view: page
title: "5. Haciendo Modificaciones"
---

<h3>Metas</h3>

<ul><li>Aprender a monitorar el estado del dir&eacute;torio de trabajo</li></ul>

<h2><em>01</em> Modificar la p&aacute;gina de “Hello, World”</h2>

<p>Vamos a adiccionar algunas tags HTML para nuestro saludo. Modifique los contenidos del archivo para:</p>

<h4 class="h4-pre">Archivo: <em>hello.html</em></h4>

<pre class="file"><strong>&lt;h1&gt;</strong>Hello, World!<strong>&lt;/h1&gt;</strong></pre>

<h2><em>02</em> Verificando el estado</h2>

<p>Veifique el estado del diret&oacute;rio de trabajo.</p>

<h4 class="h4-pre">Ejecute:</h4>

<pre class="instructions">git status</pre>

<p>Usted ver&aacute; &#8230;</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git status
# On branch master
# Changes not staged for commit:
#   (use "git add &lt;file&gt;..." to update what will be committed)
#   (use "git checkout -- &lt;file&gt;..." to discard changes in working directory)
#
#	modified:   hello.html
#
no changes added to commit (use "git add" and/or "git commit -a")</pre>

<p>O primeiro aspecto importante aqui &eacute; que o git sabe que o arquivo <code>hello.html</code> foi modificado, mas essas modifica&ccedil;&otilde;es ainda n&atilde;o sofreram commit para o reposit&oacute;rio.</p>

<p>El aspecto mas importante aqui es que git sabe que el archivo <code>hello.html</code> fu&eacute; alterado, pero esa alteraci&oacute;n a&uacute;n no sufri&oacute; un commit para el reposit&oacute;rio.</p>


<p>Otro aspecto es que el mensaje de estado ofrece consejos sobre lo que hacer en seguida. Si usted quiere agregar estas alteraciones para el reposit&oacute;rio, use <code>git add</code>. Para deshacer las modifica&ccedil;&otilde;es use <code>git checkout</code>.</p>

<h2><em>03</em> Pr&oacute;ximo...</h2>

<p>Colocando las modifica&ccedil;&otilde;es en stage.</p>
