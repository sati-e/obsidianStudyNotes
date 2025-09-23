Valor de 32 bits que divide o IP em duas partes, identificando a rede e o host dentro da rede
[[1 Internet Protocol - IPv4]]
>Para a máscara de rede, todos os 1 devem estar à esquerda, e todos os 0s a direita, sem intercalar

**Números de máscara válidos:** *(se não tiver esses números, não é mascara de rede)*
`255`, `254`, `252`, `248`, `240`, `224`, `192`, `128` e `0` 
>[!Warning] Não existe sub-rede impar, e não existe broadcast par

## CIDR - Classless Inter-Domain Routing
Utilizadas para reduzir o desperdício de IPs não utilizados *(reduzir o máximo possível da quantidade de IPs necessários)*
**Classe A:** `/8`
**Classe B:** `/16`
**Classe C:** `/24`
##### Ex cálculo:
**Máscara:** `255.0.0.0`
O CIDR será a quantidade de bits 1 que se encontram na máscara padrão:

![[Pasted image 20250923171747.png]]
**CIDR:** `/8`
**Barra menor** = rede **maior** *(mais hosts)*.
**Barra maior** = rede **menor** *(menos hosts, mais sub-redes)*.
## Sub-rede
É a divisão de uma rede maior em redes menores.
Possui endereço de rede, de host e de broadcast.
##### Como surge?
**Rede original maior:** `192.168.0.0/24` *(classe c)* com 256 endereços possíveis *(do 0 de rede ao 255, broadcast)*
**Hosts válidos:**  `192.168.0.1` a  `192.168.0.254`
1) Escolha quantos host por sub-rede, ex: 64
2) Ajuste do CIDR, para redes menores aumenta os bits, no caso, `/26`, pois possuirá 6 bits para hosts, totalizando 62 hosts por sub-rede
3) Ela então é dividida em 4 blocos de 64 endereços cada
##### Exemplo:
`192.168.0.20/26` é um dispositivo *(host)* que está na sub-rede `192.168.0.0/26`
## Salto
Variação de IPs dentro de uma sub-rede
A contagem de saltos mede o número dos dispositivos que um pacote atravessa até atingir seu destino
##### Exemplo:
`192.168.0.20/26` é um dispositivo *(host)* que está na sub-rede `192.168.0.0/26`
![[Pasted image 20250923193407.png]]
Uma máscara de classe C padrão varia de `o` a `255` IPs na rede, no exemplo ele vai de `0` a `64`

| Rede                | Host         | Broadcast       |
| ------------------- | ------------ | --------------- |
| 192.168.0`.0`       | `1` até `62` | 192.168.0`.63`  |
| 192.168.0`.64`      |              | 192.168.0`.127` |
| 192.168.0`.128`     |              | 192.168.0`.191` |
| 192.168.0`.192`     |              | 192.168.0`.255` |
| ~~192.168.0`.256`~~ |              | ~~192.168.0.~~  |

>[!Warning] Não existe sub-rede impar, e não existe broadcast par


## Máscara de sub-rede

<br>
ref: https://www.youtube.com/watch?v=INT-5Qa8Hls&list=PLAp37wMSBouCU49LV0qFbItufigjYk-sp&t=471s