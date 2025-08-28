##### Grau do vértice de um grafo:
Para um grafo G=(V, A), o grau de um vértice Vi ∈ V é igual ao número de vértices vizinhos conectados a este
###### O grau mínimo de um grafo é definido por 
σ = min {d(Vi) : Vi ∈ V};
###### O grau máximo de um grafo  é definido por 
$$Δ = max{d(Vi) : Vi ∈ V}$$
###### O grau médio de um grafo é definido por 
$$\overline{d}= \frac{\sum^{ |v| }_{ i=1 }d(Vi) }{ |V| } = \frac{d(V1)+d(V2)+d(V3)+...+d(Vn)}{|V|}$$

##### Grau de um vértice em um Grafo
###### Grafo simples
- d(v): número de vizinhos conectados a "v" = número de arestas incidentes em "v"

###### Grafo geral
- d(v): número de arestas incidentes em "v"

**TEOREMA:** para um grafo G=(V,A), tem-se 
$$\sum^{|V|}_{i=1}d(Vi) = 2|A|$$
 |A| é o número total de arestas;
	- |V| é o número total de vértices; 
	- O número da soma dos graus é igual ao dobro do número de arestas;
	
para um Grafo G, o grau em um vértice "v é dado por:
$$d(v)=n+2p$$n = n° de arestas incidentes em "v"
p = n° de laços/elos/anéis em "v"
