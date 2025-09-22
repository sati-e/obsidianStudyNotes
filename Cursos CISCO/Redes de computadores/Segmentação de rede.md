## Domínios de Broadcast e segmentação
A segmentação é uma abordagem de arquitetura que divide uma rede em vários segmentos ou sub-redes, permitindo administradores controlarem o fluxo de tráfego entre elas. 
- Melhor monitoramento
- Aumento de desempenho
- Ajuda a localizar problemas técnicos
- Aprimorar a segurança
Em uma rede LAN, dispositivos utilizam broadcast e o [[Dicionário | ARP]] para localizar outros dispositivos
Os Switches propagam broadcast, entretanto, roteadores não, quando ele recebe um broadcast ele não o encaminha por outras interfaces. Portanto, cada interface do roteador se conecta a um domínio de broadcast e as transmissões são propagadas apenas dentro desse domínio específico.
###### ⚠ Domínios de Broadcast Grandes
Uma rede que conecta vários host pode gerar problemas.
- Hosts gerando trafego de broadcasts em excesso podem afetar a rede de forma negativa, resultando em operações lentas.
A solução é reduzir o tamanho da rede, criando domínios de broadcasts menores, chamados "sub-redes"
- Reduz o tráfego e melhora o desempenho
- Implementação de políticas de segurança
**Sub-redes** podem ser criadas de várias maneiras, como por localização *(andares de um prédio)*, grupos/funções *(em uma faculdade, empresa)*, tipos de dispositivos *(impressoras, hosts...)*...