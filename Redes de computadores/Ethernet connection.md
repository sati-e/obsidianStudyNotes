## <font color="#ffffff">Ethernet - Padrão de comunicação para redes locais cabeadas</font>

 *:LiEqualNot: de wi-fi (ondas de rádio)*

Ethernet é utilizada para conectar dispositivos de redes locais (LAN) :LiArrowRight: Ele define regras e padrões para a transmissão de dados em redes de computadores, permitindo a comunicação entre **dispositivos, computadores, switches, roteadores e servidores**.

- Utiliza **cabos de par trançado** ou **fibra óptica**.
- É uma **tecnologia de rede**.
- Segue o padrão **IEEE 802.3, 802.3u**.

### <font color="#ffffff">formato dos quadros Ethernet </font>
Localização dos endereços MAC de destino e de origem, e informações adicionais, incluindo preâmbulo para sequenciamento e temporização, início do delimitador de quadro, cumprimento e tipo de quadro e sequência de verificação de quadro para detectar erros de transmissão.

- Ethernet protocol - 2 frame OSI (Enlace de dados)


>[!warning] Preciso alinhar os dispositivos conectados na internet para conseguir acessar de fato a velocidade que gostaria, para saber o formato e o tamanho, a temporização e a codificação.


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