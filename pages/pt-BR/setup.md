---
view: page
title: "1. Preparação"
---

<h3>Metas</h3>

<ul><li>Estar completamente preparado para usar o Git.</li></ul>

<h2><em>01</em> Configurando nome e endereço de e-mail</h2>

<p>Se você nunca usou git antes, o primeiro passo é configurar seu nome e endereço de email. Execute os seguintes comandos para fazer com que o git saiba seu nome e endereço de e-mail. Se o git já está instalado, pule para o fim da linha.</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git config --global user.name "Seu Nome"
git config --global user.email "seu_email@qualquercoisa.com"</pre>

<h2><em>02</em> Opções de Instalação: términos de linhas</h2>

<p>Além disso, para usuários de Unix/Mac:</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git config --global core.autocrlf input
git config --global core.safecrlf warn</pre>

<p>Para usuários do Windows:</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">git config --global core.autocrlf true
git config --global core.safecrlf warn</pre>
