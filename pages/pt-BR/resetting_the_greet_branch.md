---
view: page
title: "32. Resetando o branch style"
---

<h3>Metas</h3>

<ul><li>Resetar o branch style para o ponto anterior ao primeiro merge.</li></ul>

<h2><em>01</em> Resetando o branch style</h2>

<p>Vamos para o branch style no ponto <em>antes</em> de darmos merge com o branch master. Podemos <strong>resetar</strong> o branch para qualquer commit. Na verdade, isso faz com que o ponteiro do branch aponte para qualquer commit contido na árvore.</p>

<p>Aqui, queremos voltar no style branch para um ponto anterior ao merge com o master. Temos que encontrar o último commit antes do merge</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git checkout style
git hist</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git checkout style
Already on 'style'
$ git hist
*   645c4e6 2011-03-09 | Merged master fixed conflict. (HEAD, style) [Alexander Shvets]
|\  
| * 454ec68 2011-03-09 | Life is great! (master) [Alexander Shvets]
* |   5813a3f 2011-03-09 | Merge branch 'master' into style [Alexander Shvets]
|\ \  
| |/  
| * 6c0f848 2011-03-09 | Added README [Alexander Shvets]
* | 07a2a46 2011-03-09 | Updated index.html [Alexander Shvets]
* | 649d26c 2011-03-09 | Hello uses style.css [Alexander Shvets]
* | 1f3cbd2 2011-03-09 | Added css stylesheet [Alexander Shvets]
|/  
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>É um pouco difícil de ler, mas podemos perceber pelos dados que o commit Updated index.html foi o último no branch style anterior ao merging. Vamos resetar o style branch para esse commit.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git reset --hard &lt;hash&gt;</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git reset --hard 07a2a46
HEAD is now at 07a2a46 Updated index.html</pre>

<h2><em>02</em> Cheque o branch.</h2>

<p>Procure pelo log do branch style. Não existem commits de merge no nosso histórico.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git hist --all</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git hist --all
* 454ec68 2011-03-09 | Life is great! (master) [Alexander Shvets]
* 6c0f848 2011-03-09 | Added README [Alexander Shvets]
| * 07a2a46 2011-03-09 | Updated index.html (HEAD, style) [Alexander Shvets]
| * 649d26c 2011-03-09 | Hello uses style.css [Alexander Shvets]
| * 1f3cbd2 2011-03-09 | Added css stylesheet [Alexander Shvets]
|/  
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>
