# 2. Componentes e localização

O documento **Trunfo Atômico — Sprint 1.2.0**, na seção 4.7, prevê cinco componentes para a coleta e o envio de informações. A tabela mantém esses itens e indica onde seriam utilizados.

| Componente | Função | Local previsto |
| --- | --- | --- |
| Etiqueta RFID | Identificar cada frasco por meio de um código | Em cada frasco |
| Leitor RFID | Registrar a passagem do frasco identificado | Porta do setor |
| Sensor Geiger-Müller | Monitorar a radiação do ambiente | Sala de armazenamento |
| Sensor de temperatura e umidade | Coletar informações sobre as condições ambientais | Sala de armazenamento; posição exata ainda não definida |
| ESP32 | Receber as leituras dos dispositivos e transmitir os registros | Próximo aos dispositivos de coleta; posição exata ainda não definida |

As localizações específicas do sensor de temperatura e umidade e do ESP32 são **previsões para explicar a arquitetura**. O planejamento do grupo não determina o ponto exato de instalação desses dois componentes.

## Comunicação prevista

O ESP32 recebe as informações por interfaces compatíveis com os módulos utilizados e envia os registros pela rede Wi-Fi, utilizando MQTT. O broker encaminha as mensagens à aplicação, que organiza os dados para consulta no painel. Esses recursos de rede e software também estão previstos no documento do grupo, mas não constituem sensores adicionais.

## Observações sobre o funcionamento

A leitura RFID identifica um frasco no ponto de passagem; ela não permite afirmar sua localização contínua ou a autorização da movimentação. A autorização precisa ser verificada pela aplicação.

O Geiger-Müller representa a coleta de dados de radiação ambiental. A proposta não especifica modelo, calibração ou parâmetros de segurança para uso real. A escolha dos módulos, a montagem elétrica e a instalação física não fazem parte desta Sprint.
