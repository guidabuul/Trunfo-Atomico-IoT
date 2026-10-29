# 5. Relação com os conteúdos da disciplina

A proposta de monitoramento do Trunfo Atômico utiliza conceitos apresentados nas aulas 00 a 03 da disciplina, ministradas pelo professor Renan Rodrigues Mendes. Esses conteúdos ajudam a explicar como os dispositivos coletariam informações, como elas seriam processadas e de que forma chegariam ao painel.

## Identificação e coleta de dados

A aula 00 apresenta os fundamentos da Internet das Coisas, o uso de sensores e a comunicação entre dispositivos. O material também aborda tecnologias de identificação, com menção ao RFID. No projeto, esses conceitos aparecem nas etiquetas utilizadas para identificar os frascos e nos sensores que acompanhariam a radiação ambiental, a temperatura e a umidade.

## Processamento das informações

Na aula 01, o professor trabalha com o Arduino UNO, os pinos de entrada e saída e a sequência de entrada, processamento e saída. O grupo escolheu o ESP32 para receber os dados dos dispositivos e encaminhá-los à rede. Embora seja outro microcontrolador, sua função na arquitetura segue o princípio estudado em sala.

A aula 02 apresenta estruturas condicionais e o monitor serial. A lógica das condições ajuda a explicar as verificações previstas na aplicação: identificar uma movimentação sem autorização ou reconhecer uma leitura ambiental que precise de atenção.

Já a aula 03 aprofunda o trabalho com entradas digitais, incluindo exemplos de leitura de botões e resistores pull-up e pull-down. Esses conteúdos ajudam a compreender a conexão entre dispositivos e microcontroladores, embora os pinos e as interfaces exatas dependam dos módulos que seriam escolhidos para o projeto.

## Comunicação em rede

O envio de dados entre dispositivos faz parte dos fundamentos de IoT apresentados na disciplina. Para a arquitetura do Trunfo Atômico, o grupo definiu o uso de Wi-Fi e MQTT, com um broker responsável por encaminhar as mensagens à aplicação. Essa escolha vem do planejamento da equipe; não representa uma integração já realizada nas práticas com Arduino.

Assim, a proposta utiliza os conceitos das aulas como base para descrever uma aplicação de IoT ligada ao tema do Trunfo Atômico, sem afirmar que os equipamentos ou a comunicação já foram implementados.
