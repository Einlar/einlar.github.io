---
title: Novità
subtitle: Aggiunto il supporto al LaTeX!
layout: post
date:   2018-10-06 01:45:00 +0200
categories: welcome
icon: fa-book
comments: true
order: 100

---

***Buondì!***<br/>
Finalmente sono riuscito ad aggiungere il supporto al $$\LaTeX$$ all'interno di questo sito, grazie alla libreria 
$$\href{https://katex.org/}{\KaTeX}$$.<br/>
Perciò è possibile scrivere roba come $$a^2+b^2$$, o strafare e giungere a:

$$
\text{Boh}=
\begin{cases}
\begin{aligned}
i\hbar \frac{\partial}{\partial t}\psi(\vec{r},t) &= \left [\frac{-\hbar^2}{2\mu} \nabla^2 + V(\vec{r},t) \right ] \overbrace{\psi(\vec{r},t)}^{\text{Shish}^2}\\
0 &= \underbrace{\frac{\partial \mathcal{L}}{\partial q_i} (t, \vec{q}(t), \dot{\vec{q}}(t))}_{\text{Testoh}} - \frac{d}{dt}\frac{\partial \mathcal{L}}{\partial \dot{q}_i}(t, \vec{q}(t), \dot{\vec{q}}(t)) \quad \overbrace{i = 1,\dots,n}^{\text{Nota}_3}
\end{aligned}
\end{cases}
$$

Bisogna notare che ogni equazione è selezionabile con un semplice click, e copiandola con `CTRL+C` viene copiato il *codice* che la genera (almeno, così succede su browser decenti - ossia non *Edge*). Per esempio il disastro di sopra produrrà:
{% highlight latex %}
\text{Boh}=
\begin{cases}
\begin{aligned}
i\hbar \frac{\partial}{\partial t}\psi(\vec{r},t) &= \left [\frac{-\hbar^2}{2\mu} \nabla^2 + V(\vec{r},t) \right ]
\overbrace{\psi(\vec{r},t)}^{\text{Shish}^2}\\
0 &= \underbrace{\frac{\partial \mathcal{L}}{\partial q_i} (t, \vec{q}(t), \dot{\vec{q}}(t))}_{\text{Testoh}} - \frac{d}
{dt}\frac{\partial \mathcal{L}}{\partial \dot{q}_i}(t, \vec{q}(t), \dot{\vec{q}}(t)) \quad \overbrace{i = 1,\dots,n}^{\text{Nota}_3}
\end{aligned}
\end{cases}
{% endhighlight %}
Sono sicuro che la cosa avrà forse una certa utilità *in futuro*.

