---
view: page
title: "35. Слияние в ветку master"
---

<h3>Цели</h3>

<ul><li>Мы поддерживали соответствие ветки style с веткой master (с помощью rebase), теперь давайте сольем изменения style в ветку master.</li></ul>

<h2><em>01</em> Слияние style в master</h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git checkout master
git merge style</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git checkout master
Switched to branch 'master'
$
$ git merge style
Updating 6c0f848..6e6c76a
Fast-forward
 index.html       |    2 +-
 lib/style.css |    8 ++++++++
 lib/hello.html   |    6 ++++--
 3 files changed, 13 insertions(+), 3 deletions(-)
 create mode 100644 lib/style.css</pre>

<!-- <p>Поскольку последний коммит ветки master прямо предшествует последнему коммиту ветки style, git может выполнить ускоренное слияние-перемотку. При быстрой перемотке вперед, git просто передвигает указатель вперед, таким образом указывая на тот же коммит, что и ветка style.</p> -->
<p>Поскольку последний коммит ветке master прямо предшествует первому коммиту ветки style, git может выполнить ускоренное слияние-перемотку. При быстрой перемотке вперед, git просто передвигает указатель вперед, таким образом указывая на тот же коммит, что и ветка style (последний коммит в ветке style).

<p>При быстрой перемотке конфликтов быть не может.</p>

<h2><em>02</em> Просмотрите логи</h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions">git hist</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git hist
* 6e6c76a 2011-03-09 | Updated index.html (HEAD, master, style) [Alexander Shvets]
* 1436f13 2011-03-09 | Hello uses style.css [Alexander Shvets]
* 59da9a7 2011-03-09 | Added css stylesheet [Alexander Shvets]
* 6c0f848 2011-03-09 | Added README [Alexander Shvets]
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Теперь ветки style и master идентичны.</p>
