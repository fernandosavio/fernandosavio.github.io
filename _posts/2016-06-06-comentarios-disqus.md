---
layout: post
title: "Disqus: usando tags HTML"
excerpt: "Uma 'documentação' pessoal das tags aceitas pelo Disqus"
tags: 
  - disqus
  - comentarios
  - html

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

## &lt;spoiler&gt;
**Código**:
```html
Lorem ipsum dolor sit amet, <spoiler>consectetur</spoiler> adipiscing 
elit. Quisque quis tellus lectus.
```
**Resultado**:

![Resultado para a tag spoiler]({{ site.url }}/images/disqus/disqus_spoiler_tag.gif)

---

## &lt;a&gt;

**Código**:
```html
Lorem ipsum dolor sit amet, <a href="https://mussumipsum.com/">consectetur</a> 
adipiscing elit. Quisque quis tellus lectus.
```
**Resultado**:

![Resultado para a tag a]({{ site.url }}/images/disqus/disqus_link_tag.png)

---

## &lt;strong&gt; ou &lt;b&gt;

**Código**:
```html
Lorem ipsum dolor sit amet, <strong>consectetur</strong> adipiscing 
elit. <b>Quisque</b> quis tellus lectus.
```
**Resultado**:

![Resultado para a tag strong]({{ site.url }}/images/disqus/disqus_strong_tag.png)

---

## &lt;em&gt; ou &lt;i&gt;

**Código**:
```html
Lorem ipsum dolor sit amet, <em>consectetur</em> adipiscing 
elit. <i>Quisque</i> quis tellus lectus.
```
**Resultado**:

![Resultado para a tag em]({{ site.url }}/images/disqus/disqus_emphasis_tag.png)

---


## &lt;strike&gt; ou &lt;s&gt;

**Código**:
```html
Lorem ipsum dolor sit amet, <strike>consectetur</strike> adipiscing 
elit. <s>Quisque</s> quis tellus lectus.
```
**Resultado**:

![Resultado para a tag strike]({{ site.url }}/images/disqus/disqus_strike_tag.png)

---


## &lt;blockquote&gt;

**Código**:
```html
<blockquote>
Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
Quisque quis tellus lectus.
</blockquote>
```
**Resultado**:

![Resultado para a tag blockquote]({{ site.url }}/images/disqus/disqus_blockquote_tag.png)

---


## &lt;pre&gt; e &lt;code&gt;

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

---

*PS: as tags `<cite>`, `<span>`, `<p>`, `<caption>` e `<table>` não foram incluídas no post por não ter efeito aparente nos testes.*


[Disqus]: https://disqus.com/
[disqus_tags]: https://help.disqus.com/customer/portal/articles/466253-what-html-tags-are-allowed-within-comments-