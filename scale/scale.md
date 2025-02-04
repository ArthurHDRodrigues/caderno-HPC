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

![Gráfico](https://quickchart.io/chart?c={type:'line',data:{labels:[1,2,3,4,5,6,7,8,9,10],datasets:[{label:'Ideal',data:[1,1,1,1,1,1,1,1,1,1],borderColor:'blue'},{label:'Real',data:[1,.96,0.74,0.59,0.49,0.43,0.38,0.358,0.339,0.326,0.31],borderColor:'red'}]}})
