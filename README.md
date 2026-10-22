Etapa 3 – Registro dos resultados
Após executar o programa, copie os valores apresentados no terminal para a tabela do trabalho. O programa usa a mesma entrada para os quatro algoritmos em cada cenário.

Etapa 4 – Análise dos resultados
A seguir estão respostas orientativas. Nas questões que dependem dos números medidos, confira a tabela produzida pelo seu programa antes de concluir.

a) Qual algoritmo realizou o menor número de comparações para 10 elementos?

Observe as quatro colunas de comparações para o tamanho 10. O algoritmo com o menor valor será a resposta. Como o vetor é aleatório e os algoritmos possuem implementações diferentes, não se deve presumir um vencedor sem consultar os resultados.

b) Qual algoritmo realizou menos trocas ou movimentações?

Compare as colunas de trocas e movimentações, respeitando o critério de contagem definido. O Selection Sort costuma realizar poucas trocas efetivas, enquanto o Insertion Sort pode realizar vários deslocamentos. Entretanto, trocas e escritas não são operações idênticas, portanto essa diferença deve ser considerada na interpretação.

c) O comportamento observado para 10 elementos permaneceu semelhante quando o tamanho aumentou para 20?

Em geral, espera-se que os algoritmos mantenham tendências semelhantes, mas a quantidade de operações aumenta. Para vetores aleatórios, a posição inicial dos elementos influencia os resultados, de modo que a classificação entre os algoritmos pode mudar.

d) O que aconteceu com a quantidade de operações quando o vetor passou para 1.000 elementos?

A quantidade de operações tende a crescer bastante nos três algoritmos quadráticos. O Quick Sort normalmente apresenta crescimento mais moderado, próximo de 
nlogn em média. A diferença se torna mais significativa conforme aumenta o tamanho da entrada. 

algs4.cs.princeton.edu
+1

e) Bubble Sort, Insertion Sort e Selection Sort apresentam complexidade 
O(n2)O(n 2). Eles apresentaram exatamente a mesma quantidade de operações?

Não necessariamente. Embora os três apresentem comportamento quadrático em média ou no pior caso, suas operações são realizadas de maneiras diferentes. O Bubble Sort compara elementos adjacentes, o Insertion Sort desloca elementos para inserir a chave na posição correta e o Selection Sort procura o menor elemento restante. Por isso, os números de comparações, trocas e movimentações podem ser diferentes. 

algs4.cs.princeton.edu
+1

f) Qual algoritmo apresentou maior crescimento no número de operações?

Confira a diferença entre os resultados para 10, 20 e 1.000 elementos. Em geral, o Bubble Sort e o Insertion Sort podem apresentar crescimento quadrático expressivo em entradas aleatórias, assim como o Selection Sort. O algoritmo que apresentou o maior crescimento no seu experimento deve ser identificado pelos valores registrados, não apenas pela complexidade teórica.

g) Como o comportamento experimental do Quick Sort se diferenciou dos demais algoritmos?

O Quick Sort divide o vetor em partições a partir de um pivô e ordena essas partições recursivamente. Em média, tende a realizar menos operações que os algoritmos quadráticos para entradas grandes. Contudo, seu desempenho depende da escolha do pivô e pode chegar a 

O(n 2) no pior caso. 

MIT OpenCourseWare
+1

h) Os resultados encontrados são coerentes com as complexidades teóricas estudadas?

Se os resultados mostrarem um crescimento acentuado nas operações dos três algoritmos quadráticos e um crescimento relativamente menor no Quick Sort, serão coerentes com a teoria. Pequenas diferenças entre execuções não contradizem a complexidade assintótica, que descreve a tendência de crescimento e não uma quantidade exata de operações para cada vetor.

i) Qual algoritmo escolheria para ordenar milhares de pedidos?

Entre os quatro algoritmos estudados, escolheria o Quick Sort como opção geral para o experimento, desde que a implementação e a escolha do pivô sejam adequadas. Ele costuma apresentar desempenho médio 
O(nlogn), enquanto Bubble Sort, Insertion Sort e Selection Sort apresentam comportamento quadrático em situações típicas. Para um sistema de produção, também consideraria o método de ordenação nativo do Python, que oferece garantias de desempenho robustas.

A organização inicial interfere na quantidade de operações, mas não da mesma maneira para todos os algoritmos.
Vetor aleatório: o número de operações depende da distribuição dos valores e da posição inicial dos elementos.
Vetor já ordenado: o Insertion Sort tende a realizar poucas operações. O Bubble Sort otimizado também pode encerrar após uma única passagem sem trocas. O Selection Sort continua realizando aproximadamente 
Vetor em ordem inversa: o Insertion Sort e o Bubble Sort tendem a realizar muitas movimentações ou trocas. O Selection Sort mantém praticamente a mesma quantidade de comparações, independentemente da ordem inicial.
