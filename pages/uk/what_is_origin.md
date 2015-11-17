---
view: page
title: "39. Що таке origin?"
---

<h3>Цілі</h3>

<ul><li>Дізнатися про імена віддалених репозиторіїв.</li></ul>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git remote</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git remote
origin</pre>

<p>Ми бачимо, що клонований репозиторій знає про ім'я за замовчуванням віддаленого репозиторію. Давайте подивимося, чи можемо ми отримати більш детальну інформацію про ім'я за замовчуванням:</p>

<h4 class="h4-pre">Виконайте:</h4>

<pre class="instructions">git remote show origin</pre>

<h4 class="h4-pre">Результат:</h4>

<pre class="sample">$ git remote show origin
* remote origin
  Fetch URL: /Users/alex/Documents/Presentations/githowto/auto/hello
  Push  URL: /Users/alex/Documents/Presentations/githowto/auto/hello
  HEAD branch (remote HEAD is ambiguous, may be one of the following):
    style
    master
  Remote branches:
    style  tracked
    master tracked
  Local branch configured for 'git pull':
    master merges with remote master
  Local ref configured for 'git push':
    master pushes to master (up to date)</pre>

<p>Мы видим, что «имя по умолчанию» удаленного репозитория – оригинальное <strong>hello</strong>. Удаленные репозитории обычно размещаются на отдельной машине, возможно, централизованном сервере. Однако, как мы видим здесь,  они могут с тем же успехом указывать на репозиторий на той же машине. Нет ничего особенного в «имени по умолчанию», однако существует традиция  использовать «имя по умолчанию» на первичном централизованном репозитории (если таковой имеется)
Ми бачимо, що «ім'я за замовчуванням» віддаленого репозиторію - оригінальне <strong>hello</strong>. Віддалені репозиторії зазвичай розміщуються на окремій машині, можливо, централізованому сервері. Однак, як ми бачимо тут, вони можуть з тим самим успіхом вказувати на репозиторій на тій самій машині. Немає нічого особливого в «імені за замовчуванням», проте існує традиція використовувати «ім'я за замовчуванням» на первинному централізованому репозиторію (якщо такий є).</p>