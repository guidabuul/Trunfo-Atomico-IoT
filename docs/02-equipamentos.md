# 2. Equipamentos e localização

Para o monitoramento proposto, o grupo definiu a identificação dos frascos por RFID, a coleta de dados ambientais e o uso de um ESP32 para reunir e transmitir as informações. Os componentes previstos são:

| Componente | Função | Local previsto |
| --- | --- | --- |
| Etiqueta RFID | Identificar cada frasco por um código | Em cada frasco |
| Leitor RFID | Registrar a identificação dos frascos em um ponto de passagem | Porta do setor |
| Sensor Geiger-Müller | Monitorar a radiação ambiental | Sala de armazenamento |
| Sensor de temperatura e umidade | Medir a temperatura e a umidade do ambiente | Sala de armazenamento |
| ESP32 | Receber os dados dos dispositivos e encaminhá-los à rede | No setor, junto ao leitor RFID da porta |

Como referência para uma futura montagem, podem ser usados módulos comuns em projetos com microcontroladores: leitor RFID RC522, em que o frasco é aproximado do leitor ao passar pela porta; sensor DHT22 de temperatura e umidade; e um módulo contador Geiger-Müller.

## Funcionamento dos dispositivos

O leitor RFID registraria a identificação de um frasco quando sua etiqueta fosse detectada na porta do setor. Já os sensores acompanhariam as condições ambientais da sala de armazenamento. O ESP32 receberia esses dados e faria o envio à aplicação, conforme a comunicação descrita no documento [03 — Transmissão de dados](03-transmissao-de-dados.md).

