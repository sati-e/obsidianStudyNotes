#redes #cybersec 
Atualmente a maioria dos computadores utilizam dual stack, uma tecnologia de rede que permite o uso do IPv4 e do IPv6 em um mesmo dispositivo.
<br>
##### IPs
- Endereço lógico
- Identifica um host específico
- Há **uma parte que identifica a rede**.
- Há **uma parte que identifica o host/dispositivo** dentro dessa rede.
- A diferença principal é que **IPv6 tem 128 bits** (muito mais endereços possíveis) enquanto o **IPv4 tem 32 bits**.
- Possui [[Dicionário|máscara de sub-rede]]
Precisa ser configurado dentro da LAN, e mundialmente, para fornecer comunicações, locais e remotas.
>Um endereço IP é atribuído à conexão da [[Dicionário |interface de rede]] de um host *(identifica, fazendo com que os dispositivos saibam para onde enviar os dados)*
  - Cada pacote enviado pela internet tem um endereço IP de origem e destino

##### IPv4
- 32 bits agrupados em 4 bytes (8 bits)
Ex binário:  **11010001.10100101.11001000.00000001**
Ex decimal: **209.165.200.1**
- Hierárquico
Ex: **IP: 192.168.1.10**
-  Parte da rede: 192.168.1 → todos os dispositivos dessa rede têm essa parte igual.
- Parte do host: 10 → identifica **esse dispositivo específico** dentro da rede 192.168.1.0.
<br><br>
##### Anotações pessoais
Analogia sobre como funciona o IP e links:
- **O link** é como um mapa de um baú na internet, ele indica onde o baú está.
- **O conteúdo do baú** é o que você quer acessar
- **Você** é a pessoa que tem a chave (seu IP ou sessão), que permite **pegar o conteúdo** e trazê-lo até você.
Então: **você precisa saber onde está o baú e ter a chave certa para pegar o tesouro.**