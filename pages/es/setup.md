---
view: page
title: "1. Preparaci&oacute;n"
---

<h3>Metas</h3>

<ul><li>Estar completamente preparado para usar Git.</li></ul>

<h2><em>01</em> Configurando nombre y direccin&otilde; e-mail</h2>

<p>Si usted nunca us&oacute; git antes, el primer paso es configurar su nombre y direcci&aacute;n de e-mail. Ejecute los siguientes comandos para hacer con que git sepa su  nombre y direcci&aacute;n de e-mail. Si o git y&aacute; est&aacute; instalado, pase para el final de la li&ntilde;a.</p>

<h4 class="h4-pre">Ejecute:</h4>

<pre class="instructions">git config --global user.name "Su Nombre"
git config --global user.email "su_email@cualquiercosa.com"</pre>

<h2><em>02</em> Opciones de Instalaci&otilde;n: t&eacute;rminos de li&ntilde;as</h2>

<p>Adem&aacute;s de eso, para usu&aacute;rios de Unix/Mac:</p>

<h4 class="h4-pre">Ejecute:</h4>

<pre class="instructions">git config --global core.autocrlf input
git config --global core.safecrlf true</pre>

<p>Para usu&aacute;rios de Windows:</p>

<h4 class="h4-pre">Ejecute:</h4>

<pre class="instructions">git config --global core.autocrlf true
git config --global core.safecrlf true</pre>
