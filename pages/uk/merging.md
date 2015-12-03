---
view: page
title: "28. Злиття"
---

<h3>Цілі</h3>

<ul><li>Навчитися зливати дві відмінні гілки для перенесення змін в одну гілку.</li></ul>

<h2><em>01</em> Злиття гілок</h2>

<p>Злиття переносить зміни з двох гілок в одну. Давайте повернемося до гілки style і зіл'ємо master із style.</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git checkout style
git merge master
git hist --all</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git checkout style
Switched to branch 'style'
$ git merge master
Merge made by recursive.
 README |    1 +
 1 files changed, 1 insertions(+), 0 deletions(-)
 create mode 100644 README
$ git hist --all
*   5813a3f 2011-03-09 | Merge branch 'master' into style (HEAD, style) [Alexander Shvets]
|\  
| * 6c0f848 2011-03-09 | Added README (master) [Alexander Shvets]
* | 07a2a46 2011-03-09 | Updated index.html [Alexander Shvets]
* | 649d26c 2011-03-09 | Hello uses style.css [Alexander Shvets]
* | 1f3cbd2 2011-03-09 | Added css stylesheet [Alexander Shvets]
|/  
* 8029c07 2011-03-09 | Added index.html. [Alexander Shvets]
* 567948a 2011-03-09 | Moved hello.html to lib [Alexander Shvets]
* 6a78635 2011-03-09 | Add an author/email comment [Alexander Shvets]
* fa3c141 2011-03-09 | Added HTML header (v1) [Alexander Shvets]
* 8c32287 2011-03-09 | Added standard HTML page tags (v1-beta) [Alexander Shvets]
* 43628f7 2011-03-09 | Added h1 tag [Alexander Shvets]
* 911e8c9 2011-03-09 | First Commit [Alexander Shvets]</pre>

<p>Шляхом періодичного злиття гілки master з гілкою style ви можете переносити з master будь-які зміни і підтримувати сумісність змін style зі змінами в основній гілці.</p>

<p>Однак, це робить графіки комітів дійсно потворними. Пізніше ми розглянемо можливість перебазування, як альтернативи злиттю.</p>

<h2><em>02</em> Далі</h2>

<p>Що робити, якщо зміни в гілці master конфліктують зі змінами у style?</p>