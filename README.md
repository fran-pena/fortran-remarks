# Comentarios sobre el Fortran moderno

Estos comentarios pretenden mostrar que el Fortran no se puede definir como un lenguaje "antiguo" o "desfasado", pues presenta características que poseen los lenguajes modernos. 

## Uso actual

El Fortran sigue usándose de forma habitual en superordenadores por varias razones: su rapidez de ejecución, adaptación al cálculo paralelo y gran cantidad de código escrito en él.  

En la inmensa mayoría de los superordenadores, la tríada de compiladores para C, C++ y Fortran aparece invariablemente. Véase, por ejemplo, [[1]](https://www.osc.edu/resources/getting_started/supercomputing_faq), [[2]](https://www.cideu.org/wp-content/uploads/2019/12/compupdf.pdf).

Los centros de cálculo de altas prestaciones siguen realizando mejoras en los compiladores Fortran para adaptarlos a su hardware. Por poner ejemplos de los últimos años, podemos citar el acuerdo entre NNSA, Lawrence Livermore, Sandia y Los Alamos National Lab con NVIDIA para crear un compilador Fortran compiler diseñado para su infraestructura, [[3]](https://www.nextgov.com/modernization/2015/11/supercomputers-get-help-with-fortran/207930/); al Leibniz Supercomputing Center (LRZ) que corre habitualmente código Fortran [[4]](https://www.admin-magazine.com/mobile/HPC/Articles/Selecting-Compilers-for-a-Supercomputer) o a la empresa NAG, especializada en compiladores Fortran y sus acuerdos con IBM [[5]](https://numerical125.rssing.com/chan-21863687/latest-article2.php).

Las herramientas en dicho entorno son abundantes. En el artículo [[6]](https://www.sciencedirect.com/science/article/pii/S0167819119301759) se muestra, en la Fig. 18, las herramientas y framework de programación disponibles para cada lenguaje en entornos de cálculo de altas prestaciones. De más de 100 herramientas, el Fortran clasifica en el 10% de los lenguajes que dispone de un mayor número. Por otro lado, sigue siendo habitual la impartición de cursos de modernización de Fortran como, por ejemplo, este curso impartido en el High-Performance Computing Center de Stuttgart [[7]](https://www.hlrs.de/training/2024/ftn2).

Además, Fortran es un lenguaje ampliamente utilizado en cálculo numérico como parte del software de simulación numérica de fenómenos físicos. Por ejemplo, en el artículo [[8]](https://www.moreisdifferent.com/2015/07/16/why-physicsts-still-use-fortran/) se dice: _"Fortran is still a dominant language for the large scale simulation of physical systems, ie. for things like the astrophysical modeling of stars and galaxies, hydrodynamics codes (cf. Flash), large scale molecular dynamics, electronic structure calculation codes (cf. SIESTA), large scale climate models, etc."_

Por último, parte del sistema de clasificación de los superordenadores para entrar en la lista del TOP500 depende de la ejecución de código Fortran [[9]](https://www.top500.org/resources/frequently-asked-questions/).

## Rapidez

En la web [[10]](https://web.archive.org/web/20190210185723/https://benchmarksgame-team.pages.debian.net/benchmarksgame/faster/fortran.html) se muestran varios test de rendimiento o _benchmarks_ entre C y Fortran. Se ve el comportamiento similar entre ambos lenguajes, siendo más rápido el Fortran en algunos y el C en otros. En la misma página se pueden consultar otros test donde se evidencia que la tríada C, C++ y Fortran obtiene los mejores resultados frente a otros lenguajes.

Las mismas conclusiones se obtienen en la página [[11]](https://julialang.org/benchmarks/). En particular, se evidencia la mayor velocidad de los lenguajes compilados frente a los interpretados.

## Utilidad

El Fortran moderno posee características modernas de programación orientada a objetos que lo habilitan como vía de introducción a estos conceptos [[12]](https://gist.github.com/n-s-k/522f2669979ed6d0582b8e80cf6c95fd).

Posee características únicas para el cálculo paralelo, no tan extendidas en otros lenguajes. Por ejemplo, los _coarrays_ incluyen la paralelización de arrays directamente en el lenguaje. De hecho, los coarrays se clasfican en [[13]](https://www.top500.org/news/hpc-disruptors/) como _HPC disruptors_, es decir, _"things that might significantly change how industry deploys and uses high performance computing"_. Aparte, habría que mencionar las características de _High Performance Computing_, como `forall`, `where` o `pure`, integradas desde hace tiempo en el estándar de Fortran.

## Didáctica

Fortran no es un lenguaje "residual" en el cálculo numérico y la computación de altas prestaciones. Es importante mostrar, a los estudiantes de estas disciplinas, las diferencias entre lenguajes interpretados y compilados. En ese sentido, Fortran es un buen ejemplo de lenguaje compilado que permite introducir las características de estos (compilación, _linkado_, uso de ficheros de cabeceras, librerías, etc.) sin tener que entrar en aspectos específicos de cada lenguaje, que absorben un gran tiempo para su domino. Por ejemplo, los punteros no son estrictamente necesarios en Fortran. Como se indica en el artículo [[14]](https://www.moreisdifferent.com/2015/07/16/why-physicsts-still-use-fortran/), se considera más sencillo de aprender por estudiantes de Física que el C++.

## Apoyos

Muchas personas significadas en el mundo de la programación abogan por el uso y aprendizaje del Fortran Moderno. Por poner un ejemplo, en [[15]](https://fortran-lang.discourse.group/t/embed-a-jupyter-notebook-in-fortran-lang-org-learn/724/6) se mencionan los mensajes enviados en diciembre de 2020 por: 

- Guido van Rossum (Microsoft), creador de Python: En respuesta al mensaje de @ramalhoorg cuya traducción sería: _"Todavía no he encontrado un lenguaje que sea fácil para principiantes, práctico para profesionales y emocionante para los hackers como lo es Python._, el usuario @apaes_official indica _"Fortran was good too"_, a lo que Guido responde: `s/was/is/` (una manera de indicar que se debe cambiar el pasado por el presente).

Melissa Weber Mendonça (Quansight), desarrolladora de NumPy y defensora activa del uso de Fortran, responde al mensaje diciendo [[16]](https://x.com/melissawm/status/1334818706082426880): _"Voy a imprimir la respuesta de Guido para agregarla a cada presentación en el futuro para que la gente no se burle de mí"_.

- Fernando Pérez (U. Berkey), creador de Jupyter: _"Fortran is still highly relevant to science, and infused with new ideas"_. Fernando también menciona que Ondřej Čertík (GSI Technology), creador de SymPy, es contribuidor activo de @fortranlang.

Ondřej Čertík continúa con sus desarrollos en Fortran. Por ejemplo, en marzo de 2023, presentó en su blog _fastGPT: Faster than PyTorch in 300 lines of Fortran_ [[17]](https://ondrejcertik.com/blog/2023/03/fastgpt-faster-than-pytorch-in-300-lines-of-fortran/), donde escribe: _"Using a language like Fortran, which is oriented to the fastest possible array computations, allows to write code that is the highly performing, but still readable, because things get complicated and one must be able to maintain it."_
