---
view: page
title: "50. Divulgando o seu reposit&oacute;rio"
---

<h3>Metas</h3>

<ul><li>Aprender como configurar um servidor git para compartilhar reposit&oacute;rios.</li></ul>

<p>Existem maneiras diferentes de compartilhar um reposit&oacute;rio git na rede. Essa &eacute; a mais r&aacute;pida.</p>

<h2><em>01</em> Execute git server</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions"># (Do diret&oacute;rio de trabalho)
git daemon --verbose --export-all --base-path=.</pre>

<p>Agora, v&aacute; ao seu diret&oacute;rio de trabalho num terminal separado.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions"># (Do diret&oacute;rio de trabalho)
git clone git://localhost/hello.git network_hello
cd network_hello
ls</pre>
<p>Voc&ecirc; encontrar&aacute; uma c&oacute;pia do projeto hello.</p>

<h2><em>02</em> Mandando para o Git Daemon</h2>

<p>Se voc&ecirc; quer mover o reposit&oacute;rio para o Git Daemon, adicione a tag <code>--enable=receive-pack</code> ao comando git daemon. Tenha aten&ccedil;&atilde;o, esse servidor n&atilde;o tem autentica&ccedil;&atilde;o, ent&atilde;o qualquer um pode enviar mudan&ccedil;as para o seu reposit&oacute;rio.</p>
