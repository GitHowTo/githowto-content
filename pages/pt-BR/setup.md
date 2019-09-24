---
view: page
title: "1. Prepara&ccedil;&atilde;o"
---

<h3>Metas</h3>

<ul><li>Estar completamente preparado para usar o Git.</li></ul>

<h2><em>01</em> Configurando nome e endere&ccedil;o de e-mail</h2>

<p>Se voc&ecirc; nunca usou git antes, o primeiro passo &eacute; configurar seu nome e endere&ccedil;o de email. Execute os seguintes comandos para fazer com que o git saiba seu nome e endere&ccedil;o de e-mail. Se o git j&aacute; est&aacute; instalado, pule para o fim da linha.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git config --global user.name "Seu Nome"
git config --global user.email "seu_email@qualquercoisa.com"</pre>

<h2><em>02</em> Op&ccedil;&otilde;es de Instala&ccedil;&atilde;o: t&eacute;rminos de linhas</h2>

<p>Al&eacute;m disso, para usu&aacute;rios de Unix/Mac:</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git config --global core.autocrlf input
git config --global core.safecrlf warn</pre>

<p>Para usu&aacute;rios do Windows:</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git config --global core.autocrlf true
git config --global core.safecrlf warn</pre>
