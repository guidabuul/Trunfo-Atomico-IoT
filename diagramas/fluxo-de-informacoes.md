# Fluxo de informações

O fluxograma apresenta o caminho dos dados desde a coleta até o painel de acompanhamento. O leitor RFID registra a identificação dos frascos no ponto de passagem, enquanto os sensores coletam informações sobre o ambiente. O ESP32 recebe esses registros e os envia por Wi-Fi e MQTT ao broker, que os encaminha à aplicação.

A aplicação trata cada tipo de informação separadamente: consulta os registros de autorização quando há uma movimentação identificada como saída e verifica as condições estabelecidas para as leituras ambientais. A estimativa de decaimento segue outro caminho, usando informações da fonte e o conceito de meia-vida.

```mermaid
flowchart TD
    A["Leitor RFID"] --> C["ESP32"]
    B["Sensores ambientais"] --> C
    C --> D["Wi-Fi / MQTT"]
    D --> E["Broker MQTT"]
    E --> F["Aplicação / API"]
    F --> G{"Tipo de registro"}

    G -->|RFID| H{"Movimentação registrada como saída?"}
    H -->|Sim| I{"Existe autorização válida?"}
    H -->|Não| J["Registrar passagem"]
    I -->|Sim| J
    I -->|Não| K["Registrar ocorrência e aviso"]

    G -->|Sensores| L{"Leitura atende à condição de aviso?"}
    L -->|Sim| M["Registrar leitura e aviso"]
    L -->|Não| N["Registrar leitura"]

    J --> O["Banco de dados"]
    K --> O
    M --> O
    N --> O
    O --> P["Painel de acompanhamento"]

    Q["Consulta de uma fonte"] --> R["Aplicação: cálculo com a meia-vida"]
    R --> S["Quantidade restante estimada"]
    S --> P
```

A leitura RFID, por si só, não determina a direção da passagem nem confirma a autorização. Essas informações dependem dos registros mantidos pela aplicação. Os avisos sobre condições ambientais são exemplos do funcionamento previsto, sem parâmetros de segurança radiológica definidos.

O caminho de decaimento utiliza a quantidade inicial, a meia-vida do isótopo e o tempo decorrido. Trata-se de um cálculo teórico, independente das leituras dos sensores.
