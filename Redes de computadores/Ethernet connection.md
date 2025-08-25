## Ethernet - Padrão de comunicação para redes locais cabeadas

 de wi-fi (ondas de rádio)

_Ethernet is used to connect devices of a local network (LAN). It defines rules, patterns for data transmission on computers Network._

Allowing the communication between devices, computers, switches, routers and servers.

- Cabos de par trançado ou fibra óptica

Tecnologia de rede

Padrão IEEE 802.3, 802.3u

**O formato dos quadros Ethernet** - localização dos endereços MAC de destino e de origem, e informações adicionais, incluindo preâmbulo para sequenciamento e temporização, início do delimitador de quadro, cumprimento e tipo de quadro e sequência de verificação de quadro para detectar erros de transmissão.

- Ethernet protocol - 2 frame OSI (Enlace de dados)

<aside> 💡

Preciso alinhar os dispositivos conectados na internet para conseguir acessar de fato a velocidade que gostaria, para saber o formato e o tamanho, a temporização e a codificação.

![image.png](attachment:9d9cae58-2bce-460e-bc70-056b985bf456:image.png)

</aside>

**NIC - Network Interface Card:** Ethernet used to access LAN Ethernet.

- Have a **MAC - Media Access Control:** NIC permanent address

# Encapsulation

↳ **The process of changing _the letter_ to _the envelope_**

Um formato de mensagem é colocada em um quadro específico antes de ser enviada para a rede, fornecendo o endereço do destino e o host de origem.

Messages sending on a network needs to follow’s the specific rules in order to be sent and processed.

The De-encapsulation occurs when the process is inverted by de receiver and the message is removed from the envelope

**FRAME** - Each message is capsulated on a specific format

# Ethernet Switches

**Camada OSI:** 2 (Data Enlace)

↳ Baseado nela (que é o próprio cabeçalho da ethernet frame), tomam decisões de encaminhamento.