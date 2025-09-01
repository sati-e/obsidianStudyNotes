*Modelo teórico desenvolvido na década de 80 pela ISO que descreve como os dados são transmitidos em uma rede de computadores.*

<center>Surgiu pela necessidade de padronizar a comunicação entre sistemas abertos</center>

| OSI Layer                                                           | Description                                                                                                                                                       | Exemplos                                                                                                        | TCP/IP        |
| :------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | ------------- |
| <span style="background:rgba(3, 135, 102, 0.2)">7 - Application     | Hav</span>e the protocols used for communication process to process<br>Interface com o usuário, serviços de rede                                                  | HTTP/HTTPS(web), SMTP (email), DNS (tradução de nomes de domínio público)                                       | Application   |
| <span style="background:rgba(3, 135, 102, 0.2)">6 - Presentation    | Common re</span>presentation of data transfer on services of each layer<br>Tradução de dados, criptografia, compressão                                            | SSL/TSL (segurança na web), JPEG/PNG (imagens), MP3/MP4 (formatos de multimídia)                                | Application   |
| <span style="background:rgba(3, 135, 102, 0.2)">5 - Session         | Organizes dialogs and manage data trades                                                                                                                          | Estabelecimento de conexões em HTTPS, login persistente em sites, gerenciamento de sessões em videoconferências | Application   |
| <span style="background:rgba(5, 117, 197, 0.2)">4 - Transport       | S</span>egmentation, transfer, regroup data to individual communication between final device                                                                      | TCP (entrega confiável, usado no HTTP, email), UDP (rápido usado em jogos online, vídeos)                       | Transport     |
| <span style="background:rgba(240, 200, 0, 0.2)">3 - Network         | </span> Data trades by network between final device                                                                                                               | IP (endereçamento), ICMP (ping), roteadores                                                                     | Internet      |
| <span style="background:rgba(163, 67, 31, 0.2)">2 - Data link       | M</span>ethods for exchanging data frames between devices over a common media                                                                                     | Ethernet (cabos), Wifi (rede sem fio), Hubs e switches, PPP                                                     | Acesso a rede |
| <span style="background:rgba(163, 67, 31, 0.2)">1 - Physical</span> | Mechanical, electrical, functional and procedural means to activate, maintain and de-activate physical connection for a bit transition to and from network device | Cabos de rede (UTP, fibra optica), sinais de rádio wifi, ondas 4G/5G                                            | Acesso a rede |


![[image-2.png]]

## 1 - FÍSICA
*Transmissão dos dados pelo meio físico*
- Define que tipo de meio deve ser usado
- Responde a requisições de serviço da camada de Enlace:
	:LiCornerDownRight: **Transmissão e recepção de dados digitais (bits) entre dois dispositivos.** Os bits são convertidos em sinais elétricos ou ópticos por meio de conexão guiada ou não guiada

#### CODIFICAÇÃO DE SINAIS
***CODIFICAÇÃO DE LINHA***
***Processo de converter dados binários em sinais digitais***
- Transferência de sinais digitais e eletrônicos por meio de canais físicos
- A forma como os 0s e 1s serão "escritos" no meio físico
- Divididos em categorias

***CONVERSÃO DIGITAL-ANALÓGICA***
***Processo de mudar as características de um sinal analógico baseado nas informações de dados digitais***

- Não gerencia diretamente o meio de transmissão onde os dados trafegam
###### Funções:
- **Taxa de dados:** Número de bits enviados a cada segundo, define o tempo de duração de um bit no meio
- **Sincronização de bits:** Clocks do transmissor e do receptor devem estar sincronizados
- **Configuração da linha:** ponto-a-ponto, multiponto...
- **Topologia física:** Como os dispositivos estão conectados de modo a transformar uma rede
- **Modo de transmissão:** Simplex, half-duplex ou full-duplex

## 2 - ENLACE DE DADOS
*Garante que os dados sejam entregues sem erros e na ordem correta*
- Controle de fluxo e delimitação de quadros <font color="#7f7f7f">(início e fim do quadro)</font>
	- Restringe e coordena o número de quadros ou a quantidade de dados que o remetente pode enviar antes de aguardar uma confirmação do receptor
- Detecção e correção de erros
	- CRC <font color="#7f7f7f">(permite verificar se os dados foram corrompidos durante a transmissão)</font>
- Transmissão dos frames (quadros) <font color="#7f7f7f">(sinais digitais encapsulados em pacotes de dados)</font>
- Transforma a camada física em um link confiável

Seu **desempenho** pode ser medido por diversos parâmetros, incluindo **latência, taxa de erro e throughput**

## 3 - REDE



Referências: 
[Introdução às Redes de Computadores IFRN](https://docente.ifrn.edu.br/thiagodutra/disciplinas/materiais/introducao-as-redes-de-computadores/2019.2/07-camada-fisica-i)
[As camadas do modelo OSI ilustradas - Terminalizando a Informática](https://terminalizando.com.br/as-camadas-do-modelo-osi-ilustradas)


