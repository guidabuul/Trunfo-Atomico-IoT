# Fluxo de informações

O esquema apresenta a sequência prevista de coleta, transmissão, registro e exibição. A verificação de autorização ocorre após o recebimento da identificação RFID.

```mermaid
flowchart TD
    A["RFID e sensores"] --> B["ESP32"]
    B --> C["Rede Wi-Fi"]
    C --> D["Broker MQTT"]
    D --> E["Aplicação"]
    E --> F["Registro do evento"]
    F --> G{"Evento de saída?"}
    G -->|Sim| H{"Movimentação autorizada?"}
    H -->|Não| I["Aviso de movimentação"]
    H -->|Sim| J["Passagem registrada"]
    G -->|Não| K{"Condição ambiental fora da faixa didática?"}
    K -->|Sim| L["Aviso de condição ambiental"]
    K -->|Não| M["Leitura registrada"]
    I --> N["Painel"]
    J --> N
    L --> N
    M --> N
```

As condições são definidas exclusivamente para explicar a lógica de funcionamento. O esquema não descreve um sistema operacional instalado em hospital.
