---
view: page
title: "39. O que é origin?"
---

<h3>Metas</h3>

<ul><li>Aprender sobre os nomes dos repositórios remotos.</li></ul>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git remote</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git remote
origin</pre>

<p>Nós vemos que o repositório clonado sabe o nome do repositório remoto padrão. Para acessar mais informações sobre esse tal de origin:</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git remote show origin</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git remote show origin
* remote origin
  Fetch URL: /Users/alex/Documents/Presentations/githowto/auto/hello
  Push  URL: /Users/alex/Documents/Presentations/githowto/auto/hello
  HEAD branch (remote HEAD is ambiguous, may be one of the following):
    style
    master
  Remote branches:
    style  tracked
    master tracked
  Local branch configured for 'git pull':
    master merges with remote master
  Local ref configured for 'git push':
    master pushes to master (up to date)</pre>

<p>Nós podemos ver que o &#8220;origin&#8221; do repositório remoto é o repositório <strong>hello</strong> original. Repositórios remotos são tipocamente guardados em uma máquina separada ou em um servidor centralizado. Porém, como podemos ver, eles também podem apontar para um repositório na mesma máquina. Não tem nada especial sobre o nome &#8220;origin&#8221;, mas existe uma convenção de usá-lo para o repositório primário central (se houver algum).</p>
