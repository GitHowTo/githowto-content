---
view: page
title: "46. Repositórios bare"
---

<h3>Metas</h3>

<ul><li>Aprender como criar repositórios bare.</li></ul>

<p>Repositórios bare (sem o diretório de trabalho) são tipicamente usados para compartilhamento.</p>

<h2><em>01</em> Criando um repositório bare</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">cd ..
git clone --bare hello hello.git
ls hello.git</pre>

<p style="color:red;"><strong><span class="caps">NOTA</span>: Nós estamos agora no diretório de trabalho</strong></p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git clone --bare hello hello.git
Cloning into bare repository hello.git...
done.
$ ls hello.git
HEAD
config
description
hooks
info
objects
packed-refs
refs</pre>

<p>Tipicamente, repositórios terminados em &#8216;.git&#8217; são bare. Como você pode ver, não existe nenhum diretório de trabalho no repositório hello.git. Na verdade, ele não é nada mais que o diretório .git de um repositório que não é bare.</p>
  </div>
