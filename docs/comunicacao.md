# Comunicação e tratamento de dados

## Rede proposta
Os módulos de coleta enviam sinais ao ESP32. O controlador encaminha mensagens por uma rede Wi-Fi até um broker MQTT. A aplicação assina os tópicos pertinentes, recebe os registros e atualiza o armazenamento e o painel educativo.

## Exemplo conceitual de mensagem
```json
{
  "dispositivo": "ponto-acesso-01",
  "evento": "leitura_rfid",
  "recipiente_id": "REC-001",
  "ponto": "saida_setor",
  "data_hora": "2026-10-21T14:30:00-03:00"
}
```
*Dados fictícios utilizados apenas para explicar o formato de transmissão.*

## Processamento
1. Receber a mensagem e verificar se possui os campos esperados.
2. Registrar o horário, o dispositivo e o evento.
3. Consultar a situação autorizada de movimentação, quando o evento for uma passagem.
4. Comparar leituras ambientais às condições simuladas definidas para a demonstração.
5. Atualizar o painel e gerar avisos educativos quando uma regra for atendida.

## Cuidados para evolução futura
Uma implementação real exigiria autenticação de dispositivos, proteção do tráfego, controle de acesso ao painel, tratamento de falhas de conectividade e registro auditável dos eventos. O desenho desta Sprint não afirma que esses controles já estejam implementados.
