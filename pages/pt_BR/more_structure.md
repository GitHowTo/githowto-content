---
view: page
title: "21. Mais informação sobre a estrutura"
---

<h3>Metas</h3>

<ul><li>Adicionar mais um arquivo no nosso repositório</li></ul>

<h2><em>01</em> Adicionando index.html</h2>

<p>Vamos adicionar um arquivo <code>index.html</code> ao nosso repositório. O arquivo a seguir é perfeito para esse propósito.</p>

<h4 class="h4-pre">Arquivo: <em>index.html</em></h4>

<pre class="file">&lt;html&gt;
  &lt;body&gt;
    &lt;iframe src="lib/hello.html" width="200" height="200" /&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>Adicione o arquivo e faça um commit.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git add index.html
git commit -m "Added index.html."</pre>

<p>Agora quando você abrir <code>index.html</code>, você deverá ver uma parte da página hello em uma pequena janela.</p>
