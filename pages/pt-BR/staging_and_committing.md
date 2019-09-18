---
view: page
title: "7. Colocando em stage e fazendo commits"
---

<p>Adicionar algo ao stage no git permite que voc&ecirc; continue fazendo modifica&ccedil;&otilde;es no seu diret&oacute;rio de trabalho e, quando decidir que quer interagir com o controle de vers&atilde;o, permite que guarde as mudan&ccedil;as em pequenos commits.</p>

<p>Pense que voc&ecirc; editou tr&ecirc;s arquivos (<code>a. html</code>, <code>b. html</code> e <code>c. html</code>). Depois disso voc&ecirc; tem que fazer commit de todas as modifica&ccedil;&otilde;es para que as mudan&ccedil;as em <code>a. html</code> e <code>b. html</code> sejam um &uacute;nico commit, enquanto as mudan&ccedil;as em <code>c. html</code>, que n&atilde;o s&atilde;o logicamente relacionadas com as duas outras mudan&ccedil;as nos outros dois arquivos, sejam enviadas em um commit diferente.</p>

<p>Em teoria, voc&ecirc; pode fazer o seguinte::</p>

<pre class="instructions">git add a.html
git add b.html
git commit -m "Changes for a and b"</pre>

<pre class="instructions">git add c.html
git commit -m "Unrelated change to c"</pre>

<p>Separando a adi&ccedil;&atilde;o ao stage e o commit, voc&ecirc; pode customizar o que vai em cada commit.</p>
