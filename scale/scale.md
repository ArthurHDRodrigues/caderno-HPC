# Escalabilidade

## Speedup

**Speedup** é a razão entre o tempo serial $T_s$ e o tempo paralelo $T_p$ que um mesmo programa demora para rodar.
O tempo paralelo depende da quantidade $p$ de núcleos a aplicação está configurada para usar.

$$S(p) = \frac{T_s}{T_p}$$

Idealmente, $S(p)$ é linear.

## Eficiência

**Eficiência** mede o tempo que um processador é usado.

O tempo esperado $T_E$ assume que o speedup é linear. Ele pode ser:
* $\frac{T_s}{p}$, se o tamanho do problema é constante e se cresce o número de núcleos.
* $T_s$, se o tamanho do problema cresce linearmente em função do número de núcleos. 

$$E(p) = \frac{T_E}{T_p}$$

Note que $T_E \leq T_p$, logo $E(p) \leq 1$.

O grafico de $E(p)$ tende logaritmico.

## Lei de Amdahl

* [Wikipedia](https://pt.wikipedia.org/wiki/Lei_de_Amdahl)
* Artigo: [Amdahl’s law for multithreaded multicore processors](https://www.sciencedirect.com/science/article/abs/pii/S0743731514001142)

