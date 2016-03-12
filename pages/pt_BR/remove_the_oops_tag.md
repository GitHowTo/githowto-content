---
view: page
title: "18. Removendo a tag oops"
---

<h3>Metas</h3>

<ul><li>Remover a tag oops (limpar)</li></ul>

<h2><em>01</em> Remoção da tag oops</h2>

<p>A tag oops já fez o seu trabalho. Vamos removê-la e permitir que o coletor de lixo delete o commit referenciado.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git tag -d oops
git hist --all</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git tag -d oops
Deleted tag 'oops' (was 45fa96b)
$ git hist --all
* fa3c141 2011-03-09 | Added HTML header (HEAD, v1, master) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>A tag oops não aparecerá mais no repositório.</p>
