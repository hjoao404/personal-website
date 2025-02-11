# Visão Geral das Redes de Computadores

!!! info "Aviso"

    Este capítulo fornece apenas uma introdução básica aos conceitos de redes de computadores. Todos os detalhes e tópicos falados aqui serão abordados de forma mais aprofundada nos próximos capítulos.

## O que é uma rede computacional (computer network)?

De forma simples, uma rede computacional é um conjunto de dispositivos interligados que comunicam entre si para trocar informação. Uma rede pode ser composta por dois aspetos principais:

1. A parte física, que inclui o meio físico de conexão entre os dispositivos, como cabos de rede (Ethernet), fibra ótica ou sinais sem fios (Wi-Fi).
2. A parte lógica, que corresponde às regras e protocolos que permitem a transmissão da informação, como o TCP/IP, UDP e outros. Esses protocolos garantem que os dados sejam enviados, recebidos e interpretados corretamente pelos dispositivos na rede.

## Regras Básicas das Redes

Para garantir o bom funcionamento de uma rede, existem três princípios fundamentais:

1. Uso de protocolos comuns – Todos os dispositivos na rede devem seguir os mesmos procedimentos de comunicação. Isso significa que tanto o emissor como o recetor devem usar os mesmos protocolos (como TCP/IP, UDP, HTTP, etc.) para garantir que os dados sejam compreendidos corretamente.
2. Integridade dos dados – A informação enviada deve chegar ao destino sem erros ou corrupção. Protocolos como TCP incluem mecanismos de verificação de erros, enquanto em aplicações como streaming e chamadas VoIP, alguma perda de dados pode ser tolerada para garantir fluidez na comunicação. Mais precisão é falada em alguns capítulos à frente.
3. Identificação de remetente e destinatário – Cada dispositivo na rede deve ser capaz de reconhecer quem está a enviar e a receber os dados. Para isso, são usados identificadores como endereços IP e MAC, garantindo que a informação chega ao destino correto.

## Tipos de Redes (ordenadas por tamanho)

- PAN (Personal Area Network) – Redes muito pequenas, que conectam dispositivos pessoais num curto alcance.
Exemplo: Transferência de ficheiros entre um telemóvel e um computador via Bluetooth ou Wi-Fi Direct.

- LAN (Local Area Network) – Redes que cobrem uma área limitada, como uma casa, um escritório ou um andar de um prédio.
Exemplo: A rede da tua casa ou a de uma empresa pequena.

- WLAN (Wireless Local Area Network) – Uma LAN que usa tecnologia sem fios para a comunicação entre dispositivos.
Exemplo: O Wi-Fi da tua casa ou do café.

??? question "Dúvida esclarecida"

    A maioria das casas tem uma combinação de ligações com e sem fios. No entanto, se uma casa usa exclusivamente Wi-Fi (sem cabos Ethernet para os dispositivos), então pode ser considerada uma WLAN. Mas a maioria das casas modernas tem uma LAN híbrida (com fios + wireless).

- CAN (Campus Area Network) – Uma rede que conecta vários edifícios dentro de uma área restrita, como um campus universitário ou um parque empresarial.
Exemplo: A rede de uma universidade que liga as bibliotecas, os laboratórios e os dormitórios.

- MAN (Metropolitan Area Network) – Uma rede que cobre uma cidade ou uma grande área urbana.
Exemplo: A rede de fibra ótica usada por um município para conectar diferentes departamentos da cidade.

- WAN (Wide Area Network) – Redes que cobrem grandes distâncias, interligando LANs e MANs através da internet ou de ligações privadas. Geralmente utilizam infraestruturas de telecomunicações (como satélites, fibras óticas e ligações privadas).
Exemplo: A própria Internet é a maior WAN do mundo, pois conecta redes de todo o planeta. Outros exemplos incluem redes privadas de grandes empresas que ligam escritórios em diferentes países.



