
#Grafos

##### Grafos triviais
Grafo com apenas um vértice e nenhuma aresta.

##### Grafo vazio
Possui vértices, mas nenhuma aresta ligando-os

##### Grafo Conexo
Um **Grafo simples** possui pelo menos um caminho entre cada par de vértices
>Um grafo simples **G consiste de um conjunto finito e não vazio** V(G) de objetos chamados vértices, juntamente com um conjunto A(G) de pares não ordenados de vértices; os elementos de A(G) são chamados de arestas. Podemos representá-lo por G=(V; A), onde V=V(G) e A=A(G).
- Não direcionado
- Não ponderado
- Não possui laços
- Não possui arestas "paralelas"

![[image.png|200]]

##### Grafo Desconexo
Contrário de conexo

##### Grafo Regular
Grafo que possui o mesmo grau em todos os vértices

##### Grafo Caminho/passeio
**Passeio aberto:** Caracterizado por um passeio onde o vértice destino é distinto do vértice de origem
**Passeio fechado:** É caracterizado por um passeio onde o vértice de origem é igual ao vértice de origem
**Trilha:** Não repete aresta
**Caminho:** Qualquer sequência de arestas onde o vértice final de uma aresta é o vértice inicial da próxima
**Caminho simples:**  Quando todos os vértices são distintos *(não é possível passar duas vezes pelo mesmo vértice)*

##### Grafo Ciclo
Grafo simples fechado constituindo um grafo caminho fechado
**Simbologia:** Cn (n⋟3)

##### Grafo Roda
Grafo semelhante a Cn, adicionando-se um vértice adjacente aos "n" vértices restantes
**Simbologia:** Wn

![[Pasted image 20250904082205.png]]

##### Grafo Estrela
Grafo obtido através do grafo roda, removendo-se as arestas correspondentes de Cn
**Simbologia:** Sn
![[Pasted image 20250904082342.png]]![[Pasted image 20250904083305.png]]
Ex: Torrent, e pode ser usado para criar prioridades

##### Grafo k-cubo
Grafo com rótulos formados por uma sequência binária de tamanho "K"
**Simbologia:** Qk

##### Grafo Bipartido
Um grafo G=(V,A) é bipartido se o seu conjunto de vértices V pode ser particionado em dois subconjuntos x e y, tais que X∩Y = ∅ e X∪Y = V, onde cada aresta do conjunto A possui uma extremidade em "X" e a outra em "Y".
**Simbologia:** Kp,q (completo e incompleto)

![[Pasted image 20250904084139.png|completo]]![[Pasted image 20250904084221.png|Incompleto]]

##### Grafo Ponderado
Grafo G=(V, A) onde se associe um valor Wij, também denominado "peso", associado à aresta que conecta os vértice Vi, Vj ∈ V, pode determinar distâncias, tempos, custos...

##### Grafo Direcionado

<br>
ref: https://www.youtube.com/watch?v=m4t6D24R5k8