---
view: page
title: "23. Dentro do Git: Trabalhando diretamente com objetos do git"
---

<h3>Metas</h3>

<ul>
<li>Explorar a estrutura dos objetos do banco de dados</li>
<li>Usar hashes SHA1 para pesquisar por conteúdo no repositório</li>
</ul>

<p>Vamos examinar os objetos do git com algumas ferramentas.</p>

<h2><em>01</em> Procurando pelo último commit</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git hist --max-count=1</pre>

<p>Esse comando deve encontrar o último commit nesse repositório. A hash SHA1 provavelmente é diferente em nossos sistemas, mas você deve ver algo como isto.</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git hist --max-count=1
* 8029c07 2011-03-09 | Added index.html. (HEAD, master) [Alexander Shvets]</pre>

<h2><em>02</em> Exibição do último commit</h2>

<p>Com a hash SHA1, tal como acima...</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git cat-file -t &lt;hash&gt;
git cat-file -p &lt;hash&gt;</pre>

<p>Eu vejo isso ...</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git cat-file -t 8029c07
commit
$ git cat-file -p 8029c07
tree 096b74c56bfc6b40e754fc0725b8c70b2038b91e
parent 567948ac55daa723807c0c16e34c76797efbcbed
author Alexander Shvets &lt;alex@githowto.com&gt; 1299684476 -0500
committer Alexander Shvets &lt;alex@githowto.com&gt; 1299684476 -0500

Added index.html.</pre>

<p class="note"><strong>Nota:</strong> Se você especificar o alias como «type» e «dump», como descrito na lição correspondente, você pode entrar os comandos <code>git type</code> e <code>git dump</code> ao invés de um comando longo (que eu nunca memorizo).</p>

<p>Isso exibe o objeto de commit, que está no início do branch master.</p>

<h2><em>03</em> Busca em árvore</h2>

<p>Nós podemos exibir a árvore referenciada no commit. Isso deveria ser uma descrição do arquivo no nosso projeto (para um commit específico). Use a hash SHA1 da string da árvore listada acima.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git cat-file -p &lt;treehash&gt;</pre>

<p>Aqui está a minha árvore ...</p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git cat-file -p 096b74c
100644 blob 28e0e9d6ea7e25f35ec64a43f569b550e8386f90	index.html
040000 tree e46f374f5b36c6f02fb3e9e922b79044f754d795	lib</pre>

<p>Eu posso ver o arquivo e a pasta da lib do <code>index.html</code>.</p>

<h2><em>04</em> Exibir diretório da lib</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git cat-file -p &lt;libhash&gt;</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git cat-file -p e46f374
100644 blob c45f26b6fdc7db6ba779fc4c385d9d24fc12cf72	hello.html</pre>

<p>Tem um arquivo <code>hello.html</code>.</p>

<h2><em>05</em> Exibir o arquivo <code>hello.html</code></h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git cat-file -p &lt;hellohash&gt;</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git cat-file -p c45f26b
&lt;!-- Author: Alexander Shvets (alex@githowto.com) --&gt;
&lt;html&gt;
  &lt;head&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hello, World!&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

<p>E aí está. Objetos árvores, objetos de commits e objetos blob são exibidos diretamente do repositório do git. E isso é tudo que tem - árvores, blobs e commits.</p>

<h2><em>06</em> Explore você mesmo</h2>

<p>O repositório git pode ser explorado manualmente. Tente achar manualmente o arquivo <code>hello.html</code> original do primeiro commit com ajuda da hash SHA1 referenciada no último commit.</p>
