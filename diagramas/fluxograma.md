# Fluxograma do monitoramento

O diagrama abaixo detalha o caminho de um evento desde a identificação até a atualização do painel.

```mermaid
flowchart TD
    A["Etiqueta RFID ou sensores"] --> B["Coleta pelo ESP32"]
    B --> C["Wi-Fi"]
    C --> D["Broker MQTT"]
    D --> E["Aplicação recebe o evento"]
    E --> F["Valida e registra os dados"]
    F --> G{"Movimentação de recipiente?"}
    G -->|Sim| H{"Existe autorização registrada?"}
    H -->|Não| I["Gerar alerta educativo de saída"]
    H -->|Sim| J["Registrar passagem autorizada"]
    G -->|Não| K{"Leitura fora da condição simulada?"}
    K -->|Sim| L["Gerar aviso educativo"]
    K -->|Não| M["Registrar leitura normal no cenário"]
    I --> N["Atualizar painel"]
    J --> N
    L --> N
    M --> N
```

## Leitura do fluxograma
A coleta é realizada pelos dispositivos; a comunicação utiliza Wi-Fi e MQTT; e a interpretação dos eventos ocorre na aplicação. A simulação de autorização é uma regra do sistema, não uma capacidade do leitor RFID. O painel apresenta o resultado ao usuário.
