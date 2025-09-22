Endereços de `128 bits`
A IoT, fez crescer o número de dispositivos que acessam a internet, e o esgotamento do IPv4 é o motivador da migração para o IPv6.
Atualmente a maioria dos dispositivos utilizam dual-stack por ainda estar em transição, entretanto o ideal é a comunicação IPv6 nativa de origem até o destino.
A IETF criou alguns protocolos e ferramentas para ajudar os administradores de rede na migração:
**Dual Stack:** Permite que os dois tipos de IPs coexistam no mesmo segmento de rede, ele não converte, escolhe qual usar.
**Tunelamento:** Método de transporte de pacote IPv6 através de uma rede IPv4, encapsula o IPv6 dentro de um pacote IPv4.
**Conversão:** NAT64 e NAT46 utilizam a conversão, tradução, para a comunicação

>[!Warning] O Tunelamento e a Conversão só devem ser usadas quando necessário.

# Endereçamento
## Numeração Hexadecimal
Os IPv6 são representados em hexadecimais *(base 16 com dígitos 0 a 9 e A a F)*
##### Segmentos ou Hextets de 16 bits
`x: x: x: x: x: x: x: x` 
O IPv6 é constituído por 8 hextetos 
4 dígitos hexadecimais = 16 dígitos binários = 1 hexteto
Ele possui 128 bits, então, 128 bits :LiDivide: 4 = 35 dígitos hexadecimais
###### Reduzir tamanho
**Omitir zeros à esquerda:** A primeira forma de reduzir um endereço é omitir todos os zeros a esquerda de cada segmento.
**Ex:** 
`2001 : 0db8 : 000a : 0001 : c012 : 9aff : fe9a: 19ac`
`2001 : db8 : a : 1 : c012 : 9aff : fe9a: 19ac`
**Dois pontos duplos:** A segunda forma é, caso houver segmentos zerados, eles também sejam omitidos, deixando os dois pontos ainda sim
**Ex:**
`fe80 : 0000 : 0000 : 0000 : 0123 : 4567 : 89ab: cdef`
`fe80 : : 123 : 4567 : 89ab: cdef`
⚠ Caso existir segmentos zerados separados, a maior sequência deve ser omitida, não podendo existir duas omissões desse tipo
`fe80 : 0000 : 0000 : 0000 : 0123 : 0000 : 89ab: cdef`
`fe80 : : 123 : 0000 : 89ab: cdef`

