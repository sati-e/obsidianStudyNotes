Aresta orientada = arco
##### Grafo não direcionado
$$ [M_{ij}] = 
\left\{
\begin{array}{1}
o \\ m\\ p
\end{array}
\right.
$$
##### Grafo Direcionado
$$ [M_{ij}] = 
\left\{
\begin{array}{l}
\text{ o, vértice "i" não é adjacente ao vértice "j"}\\
\text{ m, m sendo a quantidade de arcos com origem em "i", e destino em "j"}
\end{array}
\right.
$$
**Ex:**
![[Pasted image 20251002101744.png]]
$$
Matriz =
\begin{bmatrix}
0 & 1 & 0 & 0\\
1 & 1 & 1 & 0\\
1 & 0 & 0 & 2\\
0 & 0 & 1 & 0\\
\end{bmatrix}
$$
##### Aresta Adjacente
Representação computacional de todas as arestas/arcos de um grafo na forma de lista
**Ex:**
[[]]

##### Matriz de Incidência
$$
\begin{array}{l}
\text{Dado um Grafo } G = (V, A), \\
\text{a matriz de incidência } J = [II_{ij}] \\
\text{é um conjunto de elementos matriciais com linhas e colunas que} \\
\text{associa os vértices às arestas de G, onde}
\end{array}
$$
