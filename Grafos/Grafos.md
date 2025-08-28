07-08-2025 08:22

Status: #EmProgresso 
Tags: [[3 - Tags/Faculdade | Faculdade]] #Código 


# Grafos

### Grau 
- É a quantidade vizinhos que um Vértice tem;
- O Grau de um grafo é igual a media de vizinhos entre cada vértice;
### Tamanho
- O tamanho de um grafo é o número de arestas de um grafo;

## Grafos Simples:
- Um grafo Simples G = (V,A) é uma estrutura discreta formada por um conjunto de vértices e arestas (estes representados por V e A, respectivamente), considerando que o conjunto de arestas obedeça à condição A ⊆ P(v), onde P(v) = { {x, y} : x, y ∈ v} é o conjunto de nodos os pares gerados a partir de V.
	- **{x, y}: arestas**: formados a partir dos vértices x e y, onde x != y;
	- **OBS:** para cada par de vértice existe, **NO MÁXIMO**, uma aresta associada/conectada.
![[Grafo_k4_plano.png]]
## Multigrafo:
- Um grafo G=(V, A) é dito multigrafo se,  e somente se, existir múltiplas arestas para um determinado par de vértices (Vi, Vj), onde Vi, Vj ∈ V.
 ![[Walk-trail-path.png]]
## Pseudografo:
- Um grafo G=(V, A) é dito pseudografo se, e somente se, existir pelo menos uma aresta especial que conecta um vértice Vi ∈ V a ele mesmo. Esta aresta é chamada de laço/anel/elo.
![[Pseudografo_Dirigido.png]]

## Multiplicidade:
- Para um dado par de vértices Vi, Vj ∈ V a multiplicidade deste é o número de arestas conectadas a tal par:
	- m(Vi, Vj) = K onde K é o número de arestas entre os dois;
	- Exemplo:
	- ![[Walk-trail-path.png]]
	- m(a, b) = 2 
	- m(a, c) = 1
	- m(a, d) = 1
	- m(b, c) = 1
	- m(b, d) = 1
	- m(c, d) = 1
	- m(c, g) = 1
	- m(d, g) = 1
## Grau do vértice de um grafo:
- Para um grafo G=(V, A), o grau de um vértice Vi ∈ V é igual ao número de vértices vizinhos conectados a este;
- ###### O grau mínimo de um grafo é definido por σ = min {d(Vi) : Vi ∈ V};
- ###### O grau máximo de um grafo  é definido por Δ = max{d(Vi) : Vi ∈ V};
- ###### O grau médio de um grafo é definido por $$\overline{d}= \frac{\sum^{ |v| }_{ i=1 }d(Vi) }{ |V| } = \frac{d(V1)+d(V2)+d(V3)+...+d(Vn)}{|V|}$$
- Teorema:
	- Para um grafo $$\sum^{|V|}_{i=1}d(Vi) = 2|A|$$
	- |A| é o número total de arestas;
	- |V| é o número total de vértices; 
	- O número da soma dos graus é igual ao dobro do número de arestas;
	- Teorema: para um Grafo G, o grau em um vértice "v" é dado por : $$d(v) = n+ 2p$$
		- Onde: n : número de arestas indentes em V;
		- p: número de  laços/elos/anéis em "v";
## Grafo Regular:
- Grafo que possui o mesmo **grau** (grau de um vértice é definido pela quantidade de vértices vizinhos ligados a este) em todos os seus vértices.
- ##### Grafo regular de ordem N $$N = \sigma = \Delta = \overline d$$
	- N é a ordem (ordem é o grau médio entre os vértices);
	- δ = grau mínimo
	- Δ = grau máximo
	- đ = grau médio de um grafo
## Grafo Conectado:
- Grafo que **não** pode ser expresso através da união de dois outros grafos. Por outro lado, em caso contrário, o grafo é considerado **desconectado**.

## Passeio:
- Dado um Grafo G = (V, A), com V = {V1, V2, ..., Vk} e A = {Vi Vi+1 : 1 <= i <= k-1} a sequência alternada entre vértices e arestas é denominada de **passeio**.
	- **Passeio Aberto: é caracterizado por um passeio onde o vértice destino é distinto do vértice de origem**;
	- **Passeio Fechado: é caracterizado por um passeio onde o vértice de origem é igual ao vértice destino**;
	- **Trilha: tipo de passeio caracterizado pela presença de** arestas distintas;
		- Uma trilha fechada é chamada de Circuito;
	- **Caminho: tipo de passeio caracterizado pela presença de** vértices distintos **e** arestas distintas;
		- Um caminho fechado é chamado de ciclo;
## Grafo Orientado/Direcionado
## References:
[[Grafo_k4_plano.png | Grafo Simples]]
[[Walk-trail-path.png | Multigrafo]]
[[Pseudografo_Dirigido.png | Pseudografo]]

