# Escalabilidade

## Speedup

**Speedup** é a razão entre o tempo serial $T(1)$ e o tempo paralelo $T(p)$ que um mesmo programa demora para rodar usando $p$ núcleos.

$$S(p) = \frac{T(1)}{T(p)}$$

A lei de Amdahl ([Wiki](https://pt.wikipedia.org/wiki/Lei_de_Amdahl), [Artigo](https://www.sciencedirect.com/science/article/abs/pii/S0743731514001142)) propõe um speedup ideal. Seja $B\in [0,1]$ a fração do código que necessáriamente é sequêncial, então a lei de Amdahl afirma que

$$
T(p) = T(1)(B+\frac{1-B}{p}).
$$

Logo o speedup ideal é:

$$
S(p) = \frac{1}{B+\frac{1-B}{p}}
$$

Se $B=0$, então $S(p)$ é linear em $p$, mas em alguns casos ela pode ser superlinear, como analisado [nesse artigo](https://iopscience.iop.org/article/10.1088/1757-899X/1312/1/012009) e [nesse artigo](https://annals-csis.org/proceedings/2016/pliks/498.pdf).

## Eficiência

**Eficiência** mede o tempo que um processador é usado e é dados pela seguinte formula, onde $T_E$ é o consumo de tempo esperado.

$$E(p) = \frac{T_E}{T(p)}$$

O tempo esperado $T_E$ assume que o speedup é linear. Ele pode ser:
* **Escalonamento forte**: $T_E = \frac{T(1)}{p}$, se o tamanho do problema é constante e se cresce o número de núcleos.

$$
E(p) = \frac{T_E}{T(p)} = \frac{T(1)}{pT(p)} = \frac{S(p)}{p}
$$

  Note que $T_E \leq T(p)$, logo $E(p) \leq 1$.


* **Escalonamento fraco**: $T(1)$, se o tamanho do problema cresce linearmente em função do número de núcleos. 

$$
E(p) = \frac{T_E}{T(p)} = S(p)
$$

# Recursos externos
* Artigo: [Speedup and efficiency of computational parallelization: A unifying approach and asymptotic analysis](https://www.sciencedirect.com/science/article/pii/S0743731523002058).
* Artigo: [Understanding superlinear speedup in current HPC architectures](https://iopscience.iop.org/article/10.1088/1757-899X/1312/1/012009)
* Pagina do HPC Wiki sobre [escalabilidade](https://hpc-wiki.info/hpc/Scaling), tem exemplos reais de speedup e eficiência.
* Tutorial do HPC Wiki sobre [Benchmarking & Scaling](https://hpc-wiki.info/hpc/Benchmarking_%26_Scaling_Tutorial).
