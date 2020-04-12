---
title: "Tema 3 - Límites y continuidad"
author: "Juan Gabriel Gomila, Arnau Mir y Llorenç Valverde"
date: ''
output: 
  ioslides_presentation: 
    css: Mery_style.css
    fig_caption: yes
    keep_md: yes
    logo: Images/calculus.gif
    widescreen: yes
---



# Introducción

## Funciones reales de variable real

Supondremos que son conocidos el concepto de **función**, en tanto que una **aplicación** entre conjuntos de números. En particular, nos concentraremos en **funciones reales de variable real**, es decir en funciones $f:\mathbb{R} \rightarrow \mathbb{R}$.

Tambien suponemos conocidos los cenceptos de **rango** y **dominio** de una función, así como los términos **variable independiente** y **dependiente**. 

Aunque seran tratadas con detalle más adelante, es conveniente tener presentes las principales características de funciones elementales como las polinómicas $f(x)= P_n(x) = a_nx^n+a_{n-1}x^{n-1}+ \cdots + a_1x+a_0$, la exponencial $f(x)=e^x$,  las trigonométricas $f(x)=\sin(x)$, $f(x)=\cos(x)$, $f(x) =\tan(x)$, entre otras. 

## Funciones reales de variable real

Uno de los principales objetivos del càlculo es el estudio las funciones. De hecho, como ya se ha mencionado, el **cálculo diferencial** trata del estudio de la **medida del cambio**, precisamente a través de relaciones que vienen expresadas como funciones, principalmente como **funciones reales de variable real**

La primera cuestión que se aborda tiene que ver con los **números reales**, en particular cómo **evaluar las funciones reales de variable real** cuando la **variable independiente** es un número **irraciona**l. Nuevamente el concepto de **límite** viene a ayudar en la solución de esta cuestión.

## Límite de una función en un punto

<l class="definition"> **Definición. Límite de una función en un punto.** </l>

Sea $f:A \subset \mathbb{R}$ una función definida sobre el conjunto $A \subset \mathbb{R}$ y sea $x_0$ un punto de acumulación de $A$. $L \in \mathbb{R}$ es el **límite de $f(x)$ cuando $x$ tiende a $x_0$** si para toda sucesión $\{x_n\}_{n \in \mathbb{N}}$ de puntos de $A$ tal que $\lim_{n \rightarrow \infty}x_n = x_0$ es $\lim_{n \rightarrow \infty}f(x_n)=L$.

Escribiremos, $\lim_{x \rightarrow x_0}f(x)=L$, para indicar el límite de $f(x)$ cuando $x$ tiende a $x_0$. 


##  Límite de una función en un punto
<l class="observ"> **Observaciones.** </l>

**1.** Igual que hemos hecho con las sucesiones y los números irracionales, con esta definción convertimos el problema de evaluar una función en un punto irracional en el de calcular el límite de una sucesión. 

**2.** El hecho requerir que $x_0$ sea un punto de acumulación de $A$, nos garantiza que existan sucesiones $\{x_n\}$ de puntos de $A$ tales que $\lim_{n\rightarrow \infty} x_n = x_0$ y, por lo tanto, la definición tiene sentido.

**3.** Si $x_0$ es un punto **aislado** de $A$, es decir si hay un entorno de $x_0$ en el cual no hay puntos de $A$ diferentes de $x_0$, entonces no tiene sentido hablar del límite de $f$ en ese punto.

## Límite de una función en un punto: Ejemplos.

<div class="example"> **Ejemplos**

**Ejemplo 1.** Sea $f: \mathbb{R}\rightarrow \mathbb{R}$ definida por $f(x)=x$ y sea $c \in \mathbb{R}$, entonces
$$
\lim_{x \rightarrow c} x = c
$$
puesto que para cualquier sucesión $x_n  \rightarrow c$ es obvio que $f(x_n) = x_n \rightarrow c$.

**Ejemplo 2.** Análogamente si ahora es $f(x) = \dfrac{1}{x}$ y $c \neq 0$, entonces 

$$
\lim_{x \rightarrow c} \dfrac{1}{x} = \dfrac{1}{c},
$$
puesto que si $x_n \rightarrow c$, entonces $\dfrac{1}{x} \rightarrow \dfrac{1}{c}$

</div>

## Límite de una función en un punto: Ejemplos

<div class="example"> **Ejemplos**

**Ejemplo 3.** Si $f(x) = P_n(x) = a_n x^n + a_{n-1}x^{n-1}+ \cdots + a_1 x + a_0$, entonces para todo $c \in \mathbb{R}$ es
$$
\lim_{x \rightarrow c}P_n(x) = P_n(c) = a_n c^n + a_{n-1}c^{n-1}+ \cdots + a_1 c + a_0,
$$
como se deduce fácilmente de las propiedades aritméticas de los límites de sucesiones.

**Ejemplo 4.** Igualmente, si $P_n(x)$ y $Q_m(x)$ són polinomios tales que $P_n(x_0) \ne 0$ y $Q_m(x_0) \ne 0$, entonces 
$$
\lim_{x \rightarrow x_0} \dfrac{P_n(x)}{Q_m(x)} = \dfrac{P_n(x_0)}{Q_m(x_0)}.
$$
**Ejemplo 5.** Si $f(x) = e^x$, entonces $\lim_{x \rightarrow x_0} e^x = e^{x_0}$ puesto que, como hemos demostrado, si $x_n \rightarrow x_0$, entonces $e^{x_n} \rightarrow e^{x_0}$.
</div>


## Límite de una función en un punto: Ejemplos

<div class="example"> **Ejemplos**

**Ejemplo 6.** Más interesante és el caso $\lim_{x \rightarrow 1} \dfrac{x^5-2x^3+1}{x-1}$, puesto que, en principio, para $x=1$ la función no está definida al anularse el denominador, es decir que el dominio de la función es $\mathbb{R}\setminus\{1\}$ y, por lo tanto, $1$ es un punto de acumulación del dominio.

Ahora bien, dado que el numerador también se anula en este punto, podemos simplificar la fracción por $x-1$, con lo que nos queda que $\dfrac{x^5-2x^3+1}{x-1} = x^4+x^3-x^2-x$, y por lo tanto, $\lim _{x \rightarrow 1} \dfrac{x^5-2x^3+1}{x-1} = \lim _{x \rightarrow 1} x^4+x^3-x^2-x = 0$. 
</div>

## Caracterización del límite: propiedad $\epsilon-\delta$.

<l class="prop"> **Proposición** </l>

Sea $f:A \subset \mathbb{R} \rightarrow \mathbb{R}$ una función definida sobre el conjunto $A \subset \mathbb{R}$ y sea $x_0$ un punto de acumulación de $A$. entonces son equivalentes las tres afirmaciones siguientes:

  a) $\lim_{x \rightarrow x_0}f(x)=L$
  
  b) Para todo $\epsilon >0$ existe un $\delta >0$ tal que siempre que $0<|x-x_0|< \delta$, entonces es $|f(x)-L|<\epsilon$.

  c) Para todo entorno abierto de $L$, $V_{\epsilon}(L)$, existe un entorno abierto de $x_0$, $V_{\delta} (x_0)$ tal que para todo $x \in V^*_{\delta} (x_0)$ es $f(x) \in V_{\epsilon}(L)$, donde $V^*_{\delta}= V_{\delta} \setminus \{x_0\}$, es decir el entorno reducido de $x_0$ y radio $\delta$


## Caracterización del límite: propiedad $\epsilon-\delta$

<div class="dem"> **Demostración**

 Veamos en primer lugar que 2) $\implies$ 1). Sea $x_n$ una sucesión de puntos distintos de $x_0$, tal que $x_n \rightarrow x_0$.

Supongamos que para todo $\epsilon >0$ existe $\delta >0$ tal que si $|x - x_0|< \delta$, entonces $|f(x)-L|<\epsilon$. 

Dado que $\delta >0$, existe $n_0$ tal que para todo $n > n_0$ es $|x_n - x_0|<\delta$, por lo tanto será $|f(x_n) - L| < \epsilon$, para todo $n > n_0$, por lo que, efectivamente, $f(x_n) \rightarrow L$.

</div>

## Las dos definiciones son equivalentes

<div class="dem">

Demostramos la otra implicación por contraposición, es decir usando la equivalencia $b \implies a \equiv \lnot a \implies \lnot b$. 

Suponemos, pues, que $\lim_{x \rightarrow x_0} f(x) \neq L$, es decir que hay un $\epsilon > 0$ tal que para todo $\delta >0$ existe $x_{\delta}$ tal que $|x_{\delta} - x_0|<\delta$ y $|f(x_{\delta}) - L| \geq \epsilon$. 

Se trata de ver que hay una sucesión, $\{x_n\}$ que tiene límite  $x_0$ y que $f(x_n) \not\rightarrow_{x \rightarrow x_0} L$. 

Consideremos ahora la sucesión de números positivos $\frac{1}{n}$, y los correspondientes $x_n$ tales que $|x_n-x_0|< \frac{1}{n}$, es $|f(x_n) -L | \geq \epsilon$, es decir $f(x_n) \not\rightarrow L$, en tanto que $x_n \rightarrow x_0$, que es lo que se quería demostrar.

Finalmente, en lo que se refiere al tercer apartado, es suficiente tener en cuenta que que $|x-x_0| < \delta$ si, y sólo si,  $x \in V_{\delta}(x_0)$.

</div>

## Ejemplo de la propiedad $\epsilon-\delta$

<div class="example"> **Ejemplo**


Si $f(x)=\dfrac{1}{x}$, dado un punto $c>0$, tenemos para $x>0$, 
$$
\left|\dfrac{1}{x} -\dfrac{1}{c}\right|= \left|\dfrac{1}{cx}(c-x)\right| = \dfrac{1}{cx}|c-x|
$$
Ahora, si $x$ es tal que $|x-c| <\dfrac{1}{2}c$, de tal manera que $\dfrac{1}{2}<x<\dfrac{3}{2}$, por lo que $0 < \dfrac{1}{cx} <  \dfrac{2}{c^2} \quad \text{ para } |x-c|< \dfrac{1}{2}c$.
Por lo tanto, para estos valores de $x$ tenemos que
$$
\left|\dfrac{1}{x} -\dfrac{1}{c}\right| \leq \dfrac{2}{c^2} |x-c|
$$


Ahora, dado un $\epsilon >0$ bastaá tomar $\delta = \min \left\{\dfrac{1}{2}c, \dfrac{1}{2}c^2 \epsilon \right\}$ para tener asegurado que si $|x -c|<\delta$, entonces $\left|\dfrac{1}{x} -\dfrac{1}{c}\right| < \epsilon$.

</div>


##  Ejemplo de la propiedad $\epsilon-\delta$

<div class="example"> **Ejemplo**

Veamos que $\lim_{x \rightarrow 2} \dfrac{x^3-4}{x^2+1}= \dfrac{4}{5}$
$$
\left|\dfrac{x^3-4}{x^2+1} -  \dfrac{4}{5}\right|= \left|\dfrac{5x^3-20-4x^2-4}{5(x^2+1)}\right| = \dfrac{|5x^2+6x+12|}{5(x^2+1)}|x-2|
$$
Ahora, si $|x-2|<1$, o equivalentemente, si $0<x<3$, tendremos que $\dfrac{|5x^2+6x+12|}{5(x^2+1)} \leq \dfrac{15}{2}$, puesto que el numerador es menor o igual que $15$ y el numerador mayor o igual que $2$. 

Si para un $\epsilon >0$ tomamos $\delta = \min \left\{1, \dfrac{2}{15} \epsilon \right\}$, tendremos que si $|x-2| < \delta$, entonces 
$$
\left|\dfrac{x^3-4}{x^2+1} -  \dfrac{4}{5}\right| < \epsilon
$$
que era lo que queríamos demostrar.

## Sobre la propiedad $\epsilon-\delta$

<l class="observ"> **Observaciones** </l>

**1.** La propiedad $\epsilon -\delta$, significa que dada una precisión cualquiera, $\epsilon$, para el resultado, $L$, podemos determinar la precisión, $\delta$, con la que hay que tomar la aproximación, $x$ de $c$, para tener asegurada la precisión requerida para $L$.

**2.** Los ejemplos anteriores muestran que $\delta$ puede depender de $\epsilon$, por lo que sería más apropiado escribir $\delta(\epsilon)$, lo que no se acostumbra a hacer para evitar complicar la notación en exceso, lo cual no és óbice para olvidar esta dependencia.

**3.** Los ejemplos anteriores también pueden producir la impresión, equivocada, que es más conveniente usar la primera definición de límite que la propiedad $\epsilon-\delta$, pero veremos que, en ocasiones, resulta más conveniente esta última que la primera.

## Propiedades del límite funcional


