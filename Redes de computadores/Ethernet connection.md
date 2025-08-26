## <font color="#000000">Ethernet - Padrão de comunicação para redes locais cabeadas</font>

 *:LiEqualNot: de wi-fi (ondas de rádio)*

Ethernet é utilizada para conectar dispositivos de redes locais (LAN) :LiArrowRight: Ele define regras e padrões para a transmissão de dados em redes de computadores, permitindo a comunicação entre **dispositivos, computadores, switches, roteadores e servidores**.

- Utiliza **cabos de par trançado** ou **fibra óptica**.
- É uma **tecnologia de rede**.
- Segue o padrão **IEEE 802.3, 802.3u**.

### <font color="#000000">Formato dos quadros Ethernet </font>
Localização dos endereços MAC de destino e de origem, e informações adicionais, incluindo preâmbulo para sequenciamento e temporização, início do delimitador de quadro, cumprimento e tipo de quadro e sequência de verificação de quadro para detectar erros de transmissão.

- Ethernet protocol - 2 frame OSI (Enlace de dados)

>[!warning] Preciso alinhar os dispositivos conectados na internet para conseguir acessar de fato a velocidade que gostaria, para saber o formato e o tamanho, a temporização e a codificação.

**NIC - Network Interface Card:** Ethernet used to access LAN Ethernet.

- Have a **MAC - Media Access Control:** NIC permanent address
# Encapsulation

↳ **É o processo de transformar “a carta” em “o envelope”**

Um formato de mensagem é colocada em um quadro específico, antes de serem enviadas pela rede, as mensagens são colocadas em um **quadro específico**, que contém:

- o **endereço de destino**
- o **endereço de origem**

Assim, os dados podem ser transmitidos e processados corretamente.

- **Desencapsulamento:** é o processo inverso, realizado pelo receptor, que **retira a mensagem do envelope** para que ela possa ser lida.

📌 **Frame (quadro):** cada mensagem é encapsulada em um formato específico para o tráfego na rede.

# Ethernet Switches

**Camada OSI:** 2 (Data Enlace)

↳ Baseado nela (que é o próprio cabeçalho da ethernet frame), tomam decisões de encaminhamento.