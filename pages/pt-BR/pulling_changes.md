---
view: page
title: "44. Fazendo pull e merge de modificações"
---

<h3>Metas</h3>

<ul><li>Aprender que <code>git pull</code> é idêntico a fazer <code>git fetch</code> mais <code>git merge</code>.</li></ul>

<h3>Discussão</h3>

<p>Não iremos passar por todo o processo de fazer e dar pull em uma mudança, mas queremos que vocês saibam que: </p>

<pre class="instructions">git pull</pre>

<p>é, na verdade, equivalente a fazer os seguintes passos:</p>

<pre class="instructions">git fetch
git merge origin/master</pre>
