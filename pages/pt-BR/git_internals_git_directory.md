---
view: page
title: "22. Dentro do Git: diret&oacute;rio .git "
---

<h3>Metas</h3>

<ul><li>Aprender sobre a estrutura do diret&oacute;rio <code>.git</code></li></ul>

<h2><em>01</em> O diret&oacute;rio <code>.git</code></h2>

<p>&Eacute; hora de fazer alguma pesquisa. Come&ccedil;ando pelo diret&oacute;rio ra&iacute;z do projeto...</p>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">ls -C .git</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ ls -C .git
COMMIT_EDITMSG	MERGE_RR	config		hooks		info		objects		rr-cache
HEAD		ORIG_HEAD	description	index		logs		refs</pre>

<p>Essa &eacute; uma pasta especial onde todas as coisas do git est&atilde;o. Vamos explorar o diret&oacute;rio.</p>

<h2><em>02</em> Banco de Dados de Objetos</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">ls -C .git/objects</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ ls -C .git/objects
09	24	28	45	59	6a	77	80	8c	97	af	c4	e7	info
11	27	43	56	69	6b	78	84	91	9c	b5	e4	fa	pack</pre>

<p>Voc&ecirc; deve ver v&aacute;rias pastas nomeadas com dois caracteres. As duas primeiras letras do hash sha1 do objeto armazenado no git s&atilde;o o nome dos seus diret&oacute;rios.</p>

<h2><em>03</em> Investigue os objetos do banco de dados</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">ls -C .git/objects/&lt;dir&gt;</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ ls -C .git/objects/09
6b74c56bfc6b40e754fc0725b8c70b2038b91e	9fb6f9d3a104feb32fcac22354c4d0e8a182c1</pre>

<p>Vamos dar uma olhada em uma das pastas nomeadas com dois caracteres. Devem ter arquivos com nomes de 38 caracteres. Esses arquivos contem os objetos armazenados no git. Eles s&atilde;o comprimidos e encriptados, ent&atilde;o &eacute; imposs&iacute;vel ver seu conte&uacute;do diretamente. Vamos dar uma olhada melhor no diret&oacute;rio Git.</p>

<h2><em>04</em> Arquivo Config</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">cat .git/config</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ cat .git/config
[core]
	repositoryformatversion = 0
	filemode = true
	bare = false
	logallrefupdates = true
	ignorecase = true
[user]
	name = Alexander Shvets
	email = alex@githowto.com</pre>

<p>Esse arquivo de configura&ccedil;&otilde;es &eacute; criado para cada projeto individual. Pelo menos nesse projeto, as entradas nesse arquivo v&atilde;o sobrescrever as entradas no arquivo <code>.gitconfig</code> do seu diret&oacute;rio principal.</p>

<h2><em>05</em> Branches e tags</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">ls .git/refs
ls .git/refs/heads
ls .git/refs/tags
cat .git/refs/tags/v1</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ ls .git/refs
heads
tags
$ ls .git/refs/heads
master
$ ls .git/refs/tags
v1
v1-beta
$ cat .git/refs/tags/v1
fa3c1411aa09441695a9e645d4371e8d749da1dc</pre>

<p>Arquivos no subdiret&oacute;rio de tags devem ser familiares pra voc&ecirc;. Cada arquivo corresponde a tag anteriormente criada usando o comando <code>git tag</code>. Seu conte&uacute;do n&atilde;o &eacute; nada mais que um ahsh de um commit associado &agrave; tag.</p>

<p>A pasta <em>heads</em> &eacute; quase id&ecirc;ntica e &eacute; usada n&atilde;o para tags, mas para branches. No momento, n&oacute;s s&oacute; temos um branch e tudo que voc&ecirc; v&ecirc; nessa pasta &eacute; um branch <em>master</em>.</p>

<h2><em>06</em> Arquivo HEAD</h2>

<h4 class="h4-pre">Execute:</h4>

<pre class="instructions">cat .git/HEAD</pre>

<h4 class="h4-pre">Resultado:</h4>

<pre class="sample">$ cat .git/HEAD
ref: refs/heads/master</pre>

<p>Existe uma refer&ecirc;ncia para o branch atual no arquivo HEAD. Nesse momento, ela tem que ser para o branch master.</p>
