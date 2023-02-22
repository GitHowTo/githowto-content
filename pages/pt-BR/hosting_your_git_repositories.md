---
view: page
title: "50. Divulgando o seu repositório"
---

<h3>Metas</h3>

<ul><li>Aprender como configurar um servidor git para compartilhar repositórios.</li></ul>

<p>Existem maneiras diferentes de compartilhar um repositório git na rede. Essa é a mais rápida.</p>

<h2><em>01</em> Execute git server</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions"># (Do diretório de trabalho)
git daemon --verbose --export-all --base-path=.</pre>

<p>Agora, vá ao seu diretório de trabalho num terminal separado.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions"># (Do diretório de trabalho)
git clone git://localhost/hello.git network_hello
cd network_hello
ls</pre>
<p>Você encontrará uma cópia do projeto hello.</p>

<h2><em>02</em> Mandando para o Git Daemon</h2>

<p>Se você quer mover o repositório para o Git Daemon, adicione a tag <code>--enable=receive-pack</code> ao comando git daemon. Tenha atenção, esse servidor não tem autenticação, então qualquer um pode enviar mudanças para o seu repositório.</p>
