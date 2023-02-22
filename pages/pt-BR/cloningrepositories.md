---
view: page
title: "37. Clonando repositórios"
---

<h3>Metas</h3>

<ul><li>Aprender a fazer cópias dos repositórios.</li></ul>

<p>Se você está trabalhando em grupo, é importante que você entenda os próximos 12 capítulos, porque você geralmente terá que trabalhar com repositórios clonados.</p>

<h2><em>01</em> Vá para o seu diretório de trabalho</h2>

<p>Vá para o diretório de trabalho e clone o seu repositório hello.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">cd ..
pwd
ls</pre>

<p style="color:red;"><strong><span class="caps">NOTA</span>: Agora nós estamos no diretório de trabalho.</strong></p>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ cd ..
$ pwd
/Users/alex/Documents/Presentations/githowto/auto
$ ls
hello</pre>

<p>Neste ponto você deve estar no seu diretório &#8220;de trabalho&#8221;. Ele deve conter um único repositório chamado &#8220;hello&#8221;.</p>
<h2><em>02</em> Crie um clone do repositório hello</h2>

<p>Vamos criar um clone do repositório.</p>

<h4 class="h4-pre">Execute:</h4>
<pre class="instructions">git clone hello cloned_hello
ls</pre>
<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ git clone hello cloned_hello
Cloning into cloned_hello...
done.
$ ls
cloned_hello
hello</pre>

<p>Agora devem ter dois repositórios no seu diretório de trabalho: o &#8220;hello&#8221; original e o repositório clonado, chamado &#8220;cloned_hello&#8221;.</p>
