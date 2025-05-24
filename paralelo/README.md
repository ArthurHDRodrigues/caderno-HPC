# Paralelismo

### Compartilhado

Compartilha memória. As ferramentas mais usadas são openMP e pthreads.
* Tutorial do University of Colorado sobre [openMP com C](https://curc.readthedocs.io/en/latest/programming/OpenMP-C.html)
* No C, openMP é implementado com [pragmas](https://gcc.gnu.org/onlinedocs/cpp/Pragmas.html).
* Também é usado aceleradores como GPU e FPGA.
  
### Distribuído

Em HPC, usa-se muito MPI para fazer paralelismo distribuído.
MPI permite:
* Comunicação ponto a ponto ou coletivas
* Comunicação síncrona ou assíncrona
* Topologia de rede virtual (anel, árvore, estrela, etc)


#### Recursos sobre MPI
* Tutorial do University of Colorado sobre [MPI com C](https://curc.readthedocs.io/en/latest/programming/MPI-C.html)
* Biblioteca MPI no Debian: [openmpi-bin](https://packages.debian.org/bookworm/openmpi-bin)
* Pagina sobre MPI na [HPC Wiki](https://hpc-wiki.info/hpc/MPI)
* [MPI in small Bytes](https://www.youtube.com/watch?v=giaIDk2vPxU): Vídeo da HPC-Wiki sobre MPI
* [Repositório](https://github.com/Programacao-Paralela-e-Distribuida/MPI) do curso de MPI do livro: [Programação Paralela e Distribuída](https://www.casadocodigo.com.br/products/livro-programacao-paralela)
