# Fundamentos das aulas aplicados ao projeto

## Materiais consultados
Foram analisadas as aulas 00, 01, 02 e 03 de Disruptive Architectures: IoT, IoB e Generative AI, ministradas pelo professor Renan Rodrigues Mendes. Os conteúdos de eletrônica, Arduino, Internet das Coisas e programação básica servem de referência para a proposta conceitual da Sprint 1.

## Correspondência entre teoria e proposta

| Conteúdo das aulas | Aplicação prevista no Trunfo Atômico |
| --- | --- |
| IoT: identificação de objetos | Etiqueta e leitor RFID para registro de recipientes em pontos de passagem |
| Sensores | Leitura ambiental de radiação, temperatura e umidade no cenário proposto |
| Microcontroladores | ESP32 para reunir as leituras dos dispositivos |
| Entrada, processamento e saída | Coleta de informações, avaliação de condições e apresentação de alertas |
| Entradas digitais e analógicas | Interfaces que poderão ser usadas conforme o módulo eletrônico escolhido |
| Estruturas condicionais (if/else) | Lógica conceitual para decidir quando exibir alertas |
| Monitor Serial | Recurso possível para observar registros durante uma futura etapa de prototipação |
| Redes e protocolos de IoT | Wi-Fi e MQTT previstos para transportar mensagens |
| Simulação | Representação do monitoramento sem usar equipamentos radioativos reais |

## Justificativa do uso de ESP32
As aulas apresentam Arduino UNO e citam Arduino/ESP32 no planejamento da disciplina. Foi mantido o ESP32, previsto no projeto do grupo, em razão da necessidade conceitual de comunicação Wi-Fi. A arquitetura não exige que o professor tenha demonstrado todos os módulos apresentados.

## Entrada, processamento e saída

**Entrada:** identificação RFID e dados produzidos pelos sensores.

**Processamento:** o ESP32 recebe e organiza leituras; a aplicação consulta autorizações e compara os dados com parâmetros simulados.

**Saída:** painel educativo com identificação, registros e avisos de condições fora do esperado.

## Limites desta etapa
Os exemplos de LEDs, botões, resistores, `pinMode`, `digitalRead`, `analogRead`, `digitalWrite`, `setup` e `loop` são conteúdos efetivamente trabalhados nas aulas. Não incluímos circuitos ou código dessas rotinas como parte executada do projeto: a entrega da Sprint 1 exige apenas a aplicação **conceitual** de IoT e Redes.

Os materiais consultados não fornecem especificações de instalação de sensores radiológicos, parâmetros de segurança hospitalar nem um projeto completo de integração RFID–ESP32–MQTT. Esses elementos são escolhas da **proposta do grupo**, e não implementações demonstradas nas aulas.

## Fontes utilizadas
- FIAP. *Aula 00 — IoT*: fundamentos de Internet das Coisas, sensores, identificação, processamento e comunicação.
- FIAP. *Aula 01 — IoT*: eletrônica básica, Arduino UNO, entradas e saídas, `setup()` e `loop()`.
- FIAP. *Aula 02 — IoT*: operadores, monitor serial, repetição, estruturas condicionais e entradas digitais.
- FIAP. *Aula 03 — IoT*: entradas digitais, `INPUT_PULLUP`, leitura analógica e PWM.
- FIAP. *Challenge 2026*, versão 2, pp. 29–32: requisitos e entregáveis da disciplina.
