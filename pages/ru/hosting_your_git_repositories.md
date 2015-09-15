---
view: page
title: "50. Размещение ваших git репозиториев"
---

<h3>Цели</h3>

<ul><li>Научиться настраивать git сервер для совместного использования репозиториев.</li></ul>

Есть много способов расшаривать git репозитории по сети. Вот быстрый способ.</p>

<h2><em>01</em> Запуск git сервера</h2>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions"># (From the work directory)
git daemon --verbose --export-all --base-path=.</pre>

<p>Теперь в отдельном окне терминала перейдите в ваш рабочий каталог</p>

<h4 class="h4-pre">Выполните:</h4>

<pre class="instructions"># (From the work directory)
git clone git://localhost/hello.git network_hello
cd network_hello
ls</pre>

<p>Вы увидите копию проекта hello.</p>

<h2><em>02</em> Отправка в Git Daemon</h2>

<p>Если вы хотите совершить отправку в репозиторий Git Daemon, добавьте метку <code>--enable=receive-pack</code>  к команде git daemon. Будьте осторожны, этот сервер не производит аутентификацию, поэтому любой может отправлять изменения в ваш репозиторий.</p>