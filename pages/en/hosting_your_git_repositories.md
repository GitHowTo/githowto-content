---
view: page
title: "50. Placing your git repository"
---

<h3>Goals</h3>

<ul><li>To learn how to configure git server for sharing repos.</li></ul>

<p>There are different ways to share git repository on the network. Here's the quickest way.</p>

<h2><em>01</em> Run git server</h2>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions"># (From the work directory)
git daemon --verbose --export-all --base-path=.</pre>

<p>Now, go to your working directory in a separate terminal window.</p>

<h4 class="h4-pre">Run:</h4>

<pre class="instructions"># (From the work directory)
git clone git://localhost/hello.git network_hello
cd network_hello
ls</pre>
<p>You will find a copy of the hello project.</p>

<h2><em>02</em> Sending to Git Daemon</h2>

<p>If you want to move to the repository Git Daemon, add <code>--enable=receive-pack</code> tag to git daemon command. Be attentive, this server does not perform authentication, so anyone can submit changes to your repository.</p>