---
layout: post
title: "Disqus: usando tags HTML"
excerpt: "Uma 'documentação' pessoal das tags aceitas pelo Disqus"
tags: 
  - disqus
  - comentarios
---

# Disqus: usando tags HTML


Tenho visto muita gente "alertando" seus spoilers nos comentários do [Disqus] de vários sites da seguinte maneira:

```
[SPOILERS]
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque quis tellus lectus. 
Fusce egestas magna quis ligula tempus scelerisque. Etiam risus nunc, consequat sed 
accumsan vel, rhoncus ut augue. In venenatis elit vitae urna sollicitudin suscipit. 
Mauris vulputate pharetra pellentesque. Mauris a urna nibh. Cras varius pretium erat. 
Duis neque tortor, sagittis vel volutpat vel, maximus nec dui. Mauris vel tellus dui. 
Sed sollicitudin ligula eros, vel ornare elit semper nec.
```

ou

```
Spoiler!!!!!
.
.
.
.
.
.
.
.
.
. (aqui teria um "Leia mais")
.
.
.
.
.
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque quis tellus lectus. 
Fusce egestas magna quis ligula tempus scelerisque. Etiam risus nunc, consequat sed 
accumsan vel, rhoncus ut augue. In venenatis elit vitae urna sollicitudin suscipit. 
Mauris vulputate pharetra pellentesque. Mauris a urna nibh. Cras varius pretium erat. 
Duis neque tortor, sagittis vel volutpat vel, maximus nec dui. Mauris vel tellus dui. 
Sed sollicitudin ligula eros, vel ornare elit semper nec.
```

Depois de ver estes comentários fui ao nobre amigo Google para lembrar quais são as *tags* aceitas pelo [Disqus]{:target="_blank"}. Foi onde encontrei [este post](disqus_tags){:target="_blank"} onde mostra as tags aceitas pelo [Disqus]{:target="_blank"}.

Enfim, decidi documentar aqui no meu blog para facilitar minha vida (e de mais alguém, espero) e também vou deixar um resumo dessas *features* antes de cada sessão de comentário como uma *cola* para quem for comentar aqui no blog.

Bora lá, começando pela famigerada tag `<spoiler>`!

---

## Spoiler<small>(&lt;spoiler&gt;)</small>
**Código**:
```html
Lorem ipsum dolor sit amet, <spoiler>consectetur</spoiler> adipiscing 
elit. Quisque quis tellus lectus.
```
**Resultado**:

![Resultado para a tag spoiler]({{ site.url }}/images/disqus/disqus_spoiler_tag.gif)

<!-- Lorem ipsum dolor sit amet, <spoiler>consectetur</spoiler> adipiscing elit. Quisque quis tellus lectus. -->

---

## Hyperlinks<small>(&lt;a&gt;)</small>

**Código**:
```html
Lorem ipsum dolor sit amet, <a href="https://mussumipsum.com/">consectetur</a> 
adipiscing elit. Quisque quis tellus lectus.
```
**Resultado**:

![Resultado para a tag a]({{ site.url }}/images/disqus/disqus_link_tag.png)

---

<!-- Lorem ipsum dolor sit amet, <a href="https://mussumipsum.com/">consectetur</a> adipiscing elit. Quisque quis tellus lectus. -->

## Negrito<small>(&lt;strong&gt; ou &lt;b&gt;)</small>

**Código**:
```html
Lorem ipsum dolor sit amet, <strong>consectetur</strong> adipiscing 
elit. <b>Quisque</b> quis tellus lectus.
```
**Resultado**:

<!-- Lorem ipsum dolor sit amet, <strong>consectetur</strong> adipiscing elit. Quisque quis tellus lectus. -->

![Resultado para a tag strong]({{ site.url }}/images/disqus/disqus_strong_tag.png)

---

## Itálico<small>(&lt;em&gt; ou &lt;i&gt;)</small>

**Código**:
```html
Lorem ipsum dolor sit amet, <em>consectetur</em> adipiscing 
elit. <i>Quisque</i> quis tellus lectus.
```
**Resultado**:

<!-- Lorem ipsum dolor sit amet, <strong>consectetur</strong> adipiscing elit. Quisque quis tellus lectus. -->

![Resultado para a tag em]({{ site.url }}/images/disqus/disqus_emphasis_tag.png)

---


## Riscado<small>(&lt;strike&gt; ou &lt;s&gt;)</small>

**Código**:
```html
Lorem ipsum dolor sit amet, <strike>consectetur</strike> adipiscing 
elit. <s>Quisque</s> quis tellus lectus.
```
**Resultado**:

<!-- Lorem ipsum dolor sit amet, <strike>consectetur</strike> adipiscing elit. <s>Quisque</s> quis tellus lectus. -->

![Resultado para a tag strike]({{ site.url }}/images/disqus/disqus_strike_tag.png)

---


## Citações<small>(&lt;blockquote&gt;)</small>

**Código**:
```html
<blockquote>
Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
Quisque quis tellus lectus.
</blockquote>
```
**Resultado**:

<!-- <blockquote>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque quis tellus lectus.</blockquote> -->

![Resultado para a tag blockquote]({{ site.url }}/images/disqus/disqus_blockquote_tag.png)

---


<!--

## Menções<small>(&lt;cite&gt;)</small>

**Código**:
```html
<cite>Lorem ipsum é um texto utilizado para preencher o espaço 
de texto em publicações (jornais, revistas, e websites), com a 
finalidade de verificar o lay-out, tipografia e formatação antes 
de utilizar conteúdo real.</cite>
```
**Resultado**:

<cite>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque quis tellus lectus.</cite>


## Legenda de tabela<small>(&lt;caption&gt;)</small>

```html
<table>
    <caption>Legenda da Tabela</caption>
    <tr>
        <th>Header 1</th>
        <th>Header 2</th>
        <th>Header 3</th>
    </tr>
    <tr>
        <td>Cell 1</td>
        <td>Cell 2</td>
        <td>Cell 3</td>
    </tr>
    <tr>
        <td>Cell 4</td>
        <td>Cell 5</td>
        <td>Cell 6</td>
    </tr>
</table>
```

**Resultado**:

<table>
    <caption>Legenda da Tabela</caption>
    <tr>
        <th>Header 1</th>
        <th>Header 2</th>
        <th>Header 3</th>
    </tr>
    <tr>
        <td>Cell 1</td>
        <td>Cell 2</td>
        <td>Cell 3</td>
    </tr>
    <tr>
        <td>Cell 4</td>
        <td>Cell 5</td>
        <td>Cell 6</td>
    </tr>
</table>


## Parágrafos<small>(&lt;p&gt;)</small>

*Código*:
```html
<p>Lorem ipsum dolor sit amet, consectetur adipiscing 
elit. Quisque quis tellus lectus. Fusce egestas magna 
quis ligula tempus scelerisque.</p>
```

*Resultado*:

<p>Lorem ipsum dolor sit amet, consectetur adipiscing 
elit. Quisque quis tellus lectus. Fusce egestas magna 
quis ligula tempus scelerisque.</p>



## Span<small>(&lt;span&gt;)</small>

*Código*:
```html
Lorem ipsum dolor sit amet, consectetur adipiscing 
elit. Quisque quis tellus lectus. <span>Fusce egestas 
magna quis ligula</span> tempus scelerisque.
```

*Resultado*:

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque quis tellus lectus. <span>Fusce egestas magna quis ligula</span> tempus scelerisque.

-->

## Códigos e Syntax Highlighting<small>(&lt;pre&gt; e &lt;code&gt;)</small>

*Código*:
```html
<pre><code class="python">
## Fibonacci using recursion
def fib(n):
    if n==1 or n==2:
        return 1
    return fib(n-1)+fib(n-2)

print fib(5)
</code></pre>
```

<!-- <pre><code class="python">
## Fibonacci using recursion
def fib(n):
    if n==1 or n==2:
        return 1
    return fib(n-1)+fib(n-2)

print fib(5)
</code></pre> -->


Escapando HTML nos códigos:

*Código*:
```html
<pre><code class="html">
Lorem ipsum dolor sit amet, &#60;strong&#62;consectetur&#60;/strong&#62; 
adipiscing elit. Quisque quis tellus lectus. &#60;strike&#62;Fusce 
egestas&#60;/strike&#62; magna quis ligula tempus scelerisque.
</code></pre>
```

*Resultado*:

![Resultado para a tag code]({{ site.url }}/images/disqus/disqus_code_tag.png)

<!-- <pre><code class="html">
Lorem ipsum dolor sit amet, &#60;strong&#62;consectetur&#60;/strong&#62; adipiscing elit. Quisque quis tellus lectus. &#60;strike&#62;Fusce egestas&#60;/strike&#62; magna quis ligula tempus scelerisque.
</code></pre> -->

---

*PS: as tags `<cite>`, `<span>`, `<p>`, `<caption>` e `<table>` não foram incluídas no post por não ter efeito aparente nos testes.*


[Disqus]: https://disqus.com/
[disqus_tags]: https://help.disqus.com/customer/portal/articles/466253-what-html-tags-are-allowed-within-comments-