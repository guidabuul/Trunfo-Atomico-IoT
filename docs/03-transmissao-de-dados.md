# 3. Transmissão e tratamento dos dados

## Organização da comunicação

O ESP32 recebe dados dos módulos conectados e os encaminha pela rede Wi-Fi. Foi considerado o protocolo MQTT para transmissão das mensagens a um broker. Uma aplicação inscrita nos tópicos correspondentes recebe os eventos, verifica os campos enviados e mantém os registros disponíveis para consulta.

O broker responde pelo encaminhamento das mensagens. A verificação das regras de monitoramento ocorre na aplicação, não no broker.

## Sequência de funcionamento

1. O leitor RFID identifica uma etiqueta ou um sensor produz uma leitura.
2. O ESP32 recebe a informação e organiza a mensagem.
3. A mensagem é enviada pela rede Wi-Fi ao broker MQTT.
4. A aplicação recebe o evento, identifica o dispositivo e registra os dados.
5. Quando aplicável, consulta a autorização da movimentação ou verifica a condição ambiental prevista.
6. O painel apresenta o registro e eventual aviso.

## Exemplo de registro

```json
{
  "dispositivo": "leitor-porta-01",
  "evento": "passagem",
  "recipiente": "REC-001",
  "local": "saida-setor",
  "instante": "2026-10-21T14:30:00-03:00"
}
```

O exemplo é fictício e demonstra somente uma possível estrutura de dados. Não corresponde a uma medição ou transmissão realizada.

## Aspectos a considerar em uma futura implementação

A disponibilidade da rede, a confirmação do recebimento, a identificação de dispositivos, as permissões de acesso e o registro de falhas precisariam ser definidos e testados. Não se afirma que esses controles estejam implementados na Sprint 1.
