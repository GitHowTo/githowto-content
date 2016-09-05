---
view: page
title: "7. Colocando em stage e fazendo commits"
---

<p>Adicionar algo ao stage no git permite que você continue fazendo modificações no seu diretório de trabalho e, quando decidir que quer interagir com o controle de versão, permite que guarde as mudanças em pequenos commits.</p>

<p>Pense que você editou três arquivos (<code>a. html</code>, <code>b. html</code> e <code>c. html</code>). Depois disso você tem que fazer commit de todas as modificações para que as mudanças em <code>a. html</code> e <code>b. html</code> sejam um único commit, enquanto as mudanças em <code>c. html</code>, que não são lógicamente relacionadas com as duas outras mudanças nos outros dois arquivos, sejam enviadas em um commit diferente.</p>

<p>Em teoria, você pode fazer o seguinte::</p>

<pre class="instructions">git add a.html
git add b.html
git commit -m "Changes for a and b"</pre>

<pre class="instructions">git add c.html
git commit -m "Unrelated change to c"</pre>

<p>Separando a adição ao stage e o commit, você pode customiza o que vai em cada commit.</p>
