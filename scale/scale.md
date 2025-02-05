# Escalabilidade

## Speedup

**Speedup** é a razão entre o tempo serial $T_s$ e o tempo paralelo $T_p$ que um mesmo programa demora para rodar.
O tempo paralelo depende da quantidade $p$ de núcleos a aplicação está configurada para usar.

$$S(p) = \frac{T_s}{T_p}$$

Idealmente, $S(p)$ é linear, mas em alguns casos ela pode ser superlinear, como analisado [nesse artigo](https://iopscience.iop.org/article/10.1088/1757-899X/1312/1/012009).

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

# Recursos externos
* Artigo: [Speedup and efficiency of computational parallelization: A unifying approach and asymptotic analysis](https://www.sciencedirect.com/science/article/pii/S0743731523002058).
* Artigo: [Understanding superlinear speedup in current HPC architectures](https://iopscience.iop.org/article/10.1088/1757-899X/1312/1/012009)
* Pagina do HPC Wiki sobre [escalabilidade](https://hpc-wiki.info/hpc/Scaling), tem exemplos reais de speedup e eficiência.
* Tutorial do HPC Wiki sobre [Benchmarking & Scaling](https://hpc-wiki.info/hpc/Benchmarking_%26_Scaling_Tutorial).
