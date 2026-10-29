# 2. Equipamentos e localização

Para o monitoramento proposto, o grupo definiu a identificação dos frascos por RFID, a coleta de dados ambientais e o uso de um ESP32 para reunir e transmitir as informações. Os componentes previstos são:

| Componente | Função | Local previsto |
| --- | --- | --- |
| Etiqueta RFID | Identificar cada frasco por um código | Em cada frasco |
| Leitor RFID | Registrar a identificação dos frascos em um ponto de passagem | Porta do setor |
| Sensor Geiger-Müller | Monitorar a radiação ambiental | Sala de armazenamento |
| Sensor de temperatura e umidade | Medir a temperatura e a umidade do ambiente | Sala de armazenamento, como sugestão de instalação |
| ESP32 | Receber os dados dos dispositivos e encaminhá-los à rede | No setor, em posição a definir conforme as conexões |

A localização da etiqueta, do leitor RFID e do sensor Geiger-Müller consta do planejamento do Trunfo Atômico 1.2.0. Para o sensor de temperatura e umidade e o ESP32, o grupo ainda não definiu os pontos exatos de instalação. Os locais indicados na tabela são sugestões para explicar o funcionamento da proposta.

## Funcionamento dos dispositivos

O leitor RFID registraria a identificação de um frasco quando sua etiqueta fosse detectada na porta do setor. Já os sensores acompanhariam as condições ambientais da sala de armazenamento. O ESP32 receberia esses dados e faria o envio à aplicação, conforme a comunicação descrita no documento [03 — Transmissão de dados](03-transmissao-de-dados.md).

A identificação por RFID não informa, sozinha, a direção do movimento nem se a passagem foi autorizada. Para emitir um aviso de saída sem autorização, a aplicação precisaria consultar os registros de movimentação previstos para o sistema.

## Limites desta etapa

A Sprint 1 não exige definir marcas e modelos dos módulos, pinos de conexão ou montagem elétrica. Também não envolve medições reais. Os equipamentos foram selecionados para a descrição da arquitetura e não constituem uma instalação de monitoramento radiológico em funcionamento.
