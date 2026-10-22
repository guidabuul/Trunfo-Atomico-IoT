# Fluxo de informações

O fluxo abaixo apresenta o caminho percorrido pelos registros, desde a coleta até a consulta no painel. Após o recebimento da mensagem, a aplicação trata separadamente a identificação por RFID e as leituras dos sensores ambientais.

```mermaid
flowchart TD
    A["Leitor RFID"] --> C["ESP32"]
    B["Sensores ambientais"] --> C
    C --> D["Rede Wi-Fi"]
    D --> E["Broker MQTT"]
    E --> F["Aplicação"]
    F --> G{"Tipo de registro"}

    G -->|RFID| H{"Passagem pela saída?"}
    H -->|Sim| I{"Autorização registrada?"}
    H -->|Não| J["Registrar passagem"]
    I -->|Sim| J
    I -->|Não| K["Registrar ocorrência e aviso"]

    G -->|Sensor| L{"Condição fora da faixa didática?"}
    L -->|Sim| M["Registrar leitura e aviso"]
    L -->|Não| N["Registrar leitura"]

    J --> O["Armazenamento"]
    K --> O
    M --> O
    N --> O
    O --> P["Painel de acompanhamento"]
```

## Interpretação dos registros

A leitura RFID informa a identificação de um recipiente em um ponto específico. A verificação da autorização de movimentação depende de informação cadastrada na aplicação. Os sensores ambientais são tratados em um fluxo próprio, sem associação automática a uma passagem de recipiente.

As condições de aviso têm finalidade didática. O diagrama representa a arquitetura proposta pelo grupo, não uma instalação hospitalar em funcionamento.
