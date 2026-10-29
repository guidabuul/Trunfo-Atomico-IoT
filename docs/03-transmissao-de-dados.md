# 3. Transmissão e tratamento dos dados

## Comunicação entre os equipamentos

Na arquitetura proposta, o leitor RFID registra a identificação de uma etiqueta quando um frasco passa pelo ponto de controle. Os sensores Geiger-Müller e de temperatura e umidade coletam informações sobre o ambiente.

O ESP32 recebe esses dados por conexões compatíveis com cada dispositivo. O planejamento do grupo considera o uso de entradas digitais e analógicas, conforme o tipo de sensor. Como os modelos dos equipamentos ainda não foram definidos, a proposta não especifica pinos nem detalhes da montagem elétrica.

## Envio pela rede

Depois de receber as informações, o ESP32 as encaminharia por **Wi-Fi**, utilizando o protocolo **MQTT**. As mensagens chegariam a um broker MQTT, responsável por distribuí-las à aplicação que faria o processamento.

A comunicação seguiria este caminho:

**Leitor RFID e sensores → ESP32 → Wi-Fi e MQTT → Broker MQTT → Aplicação/API → Banco de dados → Painel.**

O broker faz o encaminhamento das mensagens. A análise dos registros e a verificação das condições de aviso ficariam a cargo da aplicação.

## Processamento e apresentação

A aplicação armazenaria os registros recebidos e os disponibilizaria para consulta no painel. No caso do RFID, uma passagem identificada como saída precisaria ser confrontada com as autorizações cadastradas. Se não houvesse autorização válida, o sistema poderia apresentar um aviso.

As leituras dos sensores ambientais também seriam registradas. No cenário proposto, a aplicação poderia indicar alterações na radiação ambiental e apresentar os valores de temperatura e umidade. Os critérios usados para gerar esses avisos não foram definidos para uma instalação real.

Esse processo permite acompanhar informações coletadas em pontos diferentes e reunir os resultados em uma mesma interface. O caminho completo, incluindo as verificações de cada tipo de registro, está representado no [fluxograma de informações](../diagramas/fluxo-de-informacoes.md).

## Limites da proposta

A documentação descreve como a comunicação funcionaria, mas não apresenta uma rede instalada ou mensagens transmitidas por equipamentos reais. O formato das mensagens, os tópicos MQTT e as configurações de conexão dependeriam da escolha dos módulos e de uma implementação futura.
