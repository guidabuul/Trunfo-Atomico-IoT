# Componentes e locais previstos

| Componente | Função | Local previsto |
| --- | --- | --- |
| Etiqueta RFID | Fornecer identificador do recipiente | Fixada no recipiente ou em sua identificação externa compatível |
| Leitor RFID | Detectar a etiqueta no ponto de passagem | Acesso ao setor |
| ESP32 | Receber sinais e encaminhar registros | Ponto de controle, em caixa apropriada |
| Detector Geiger-Müller | Fornecer leitura de radiação ambiental no cenário | Local definido para monitoramento ambiental |
| Sensor de temperatura e umidade | Registrar as condições ambientais | Sala de armazenamento |
| Ponto de acesso Wi-Fi | Dar conectividade ao ESP32 | Rede local |
| Broker MQTT | Receber e distribuir mensagens | Servidor da proposta |
| Aplicação e painel | Processar, armazenar e apresentar eventos | Ambiente lógico do sistema |

## Observações
O uso de RFID não comprova a identidade de quem movimentou o recipiente e não substitui controle de acesso. Uma avaliação de autorização exige registros e regras adicionais no sistema.

O ESP32 pode receber dados por interfaces adequadas a cada módulo (como GPIO ou comunicação serial/digital); a interface exata depende dos dispositivos escolhidos em uma eventual implementação.

O detector Geiger-Müller aqui exemplifica um sensor. Uma instalação real exigiria instrumento compatível com o tipo de radiação, calibrado e validado. Não são definidos neste projeto limites operacionais de dose ou de segurança.
