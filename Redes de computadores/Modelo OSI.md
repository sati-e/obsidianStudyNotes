*Modelo teórico desenvolvido na década de 80 pela ISO que descreve como os dados são transmitidos em uma rede de computadores.*

| OSI Layer        | Description                                                                                                                                                       |
| :--------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 7 - Application  | Have the protocols used for communication process to process                                                                                                      |
| 6 - Presentation | Common representation of data transfer on services of each layer                                                                                                  |
| 5 - Session      | Organizes dialogs and manage data trades                                                                                                                          |
| 4 - Transport    | Segmentation, transfer, regroup data to individual communication between final device                                                                             |
| 3 - Network      | Data trades by network between final device                                                                                                                       |
| 2 - Data link    | Methods for exchanging data frames between devices over a common media                                                                                            |
| 1 - Physical     | Mechanical, electrical, functional and procedural means to activate, maintain and de-activate physical connection for a bit transition to and from network device |
## 1 - FÍSICA
*Transmissão dos dados pelo meio físico*
- TCP/IP: Física, junto com a de enlace de dados
- Define que tipo de meio deve ser usado
- Responde a requisições de serviço da camada de Enlace:
	:LiCornerDownRight: **Transmissão e recepção de dados digitais (bits) entre dois dispositivos.** Os bits são convertidos em sinais elétricos ou ópticos por meio de conexão guiada ou não guiada

### CODIFICAÇÃO DE SINAIS

***CODIFICAÇÃO DE LINHA***
***Processo de converter dados binários em sinais digitais***
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







Referências: 
[Introdução às Redes de Computadores IFRN](https://docente.ifrn.edu.br/thiagodutra/disciplinas/materiais/introducao-as-redes-de-computadores/2019.2/07-camada-fisica-i)