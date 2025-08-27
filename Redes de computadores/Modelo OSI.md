*Modelo teórico desenvolvido na década de 80 pela ISO que descreve como os dados são transmitidos em uma rede de computadores.*

<center>Surgiu pela necessidade de padronizar a comunicação entre sistemas abertos</center>

| OSI Layer                                                           | Description                                                                                                                                                       | Exemplos                                               |
| :------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------ |
| <span style="background:rgba(3, 135, 102, 0.2)">7 - Application     | Hav</span>e the protocols used for communication process to process                                                                                               | HTTP/HTTPS(web), SMTP (email), DNS (tradução de nomes) |
| <span style="background:rgba(3, 135, 102, 0.2)">6 - Presentation    | Common re</span>presentation of data transfer on services of each layer                                                                                           |                                                        |
| <span style="background:rgba(3, 135, 102, 0.2)">5 - Session         | Organizes dialogs and manage data trades                                                                                                                          |                                                        |
| <span style="background:rgba(5, 117, 197, 0.2)">4 - Transport       | S</span>egmentation, transfer, regroup data to individual communication between final device                                                                      |                                                        |
| <span style="background:rgba(240, 200, 0, 0.2)">3 - Network         | </span> Data trades by network between final device                                                                                                               |                                                        |
| <span style="background:rgba(163, 67, 31, 0.2)">2 - Data link       | M</span>ethods for exchanging data frames between devices over a common media                                                                                     |                                                        |
| <span style="background:rgba(163, 67, 31, 0.2)">1 - Physical</span> | Mechanical, electrical, functional and procedural means to activate, maintain and de-activate physical connection for a bit transition to and from network device |                                                        |
## 1 - FÍSICA
*Transmissão dos dados pelo meio físico*
- TCP/IP: Física, junto com a de enlace de dados
- Define que tipo de meio deve ser usado
- Responde a requisições de serviço da camada de Enlace:
	:LiCornerDownRight: **Transmissão e recepção de dados digitais (bits) entre dois dispositivos.** Os bits são convertidos em sinais elétricos ou ópticos por meio de conexão guiada ou não guiada

### CODIFICAÇÃO DE SINAIS
***CODIFICAÇÃO DE LINHA***
***Processo de converter dados binários em sinais digitais***
- Transferência de sinais digitais e eletrônicos por meio de canais físicos
- A forma como os 0s e 1s serão "escritos" no meio físico
- Divididos em categorias

***CONVERSÃO DIGITAL-ANALÓGICA***
***Processo de mudar as características de um sinal analógico baseado nas informações de dados digitais***

- Não gerencia diretamente o meio de transmissão onde os dados trafegam
#### <u>FUNÇÕES</u>:
- **Taxa de dados:** Número de bits enviados a cada segundo, define o tempo de duração de um bit no meio
- **Sincronização de bits:** Clocks do transmissor e do receptor devem estar sincronizados
- **Configuração da linha:** ponto-a-ponto, multiponto...
- **Topologia física:** Como os dispositivos estão conectados de modo a transformar uma rede
- **Modo de transmissão:** Simplex, half-duplex ou full-duplex

## 2 - ENLACE DE DADOS
*Garante que os dados sejam entregues sem erros e na ordem correta*
- Transmissão dos frames (quadros) <font color="#7f7f7f">(sinais digitais encapsulados em pacotes de dados)</font>
- Transforma a camada física em um link confiável



Referências: 
[Introdução às Redes de Computadores IFRN](https://docente.ifrn.edu.br/thiagodutra/disciplinas/materiais/introducao-as-redes-de-computadores/2019.2/07-camada-fisica-i)