# Regras e alertas educativos

| Situação observada | Verificação prevista | Resultado no painel |
| --- | --- | --- |
| Leitura RFID na saída | Consultar autorização registrada para o recipiente naquele movimento | Aviso de saída sem autorização, se não houver registro válido |
| Leitura ambiental | Comparar com parâmetros fictícios definidos na demonstração | Aviso de condição fora do cenário esperado |
| Temperatura ou umidade | Comparar com faixa didática cadastrada | Indicador de atenção |
| Tempo decorrido de um isótopo | Aplicar cálculo de meia-vida à quantidade inicial informada | Estimativa teórica de quantidade restante |

## Critérios de interpretação
- A leitura RFID identifica uma passagem no ponto de leitura, não a posição exata e contínua do recipiente.
- Um alerta de saída não autorizada depende de uma consulta às permissões cadastradas; RFID não determina autorização sozinho.
- Leituras de radiação ambiental e estimativas de decaimento são informações diferentes.
- Os parâmetros apresentados na atividade são **fictícios e educativos**; não são limites de radioproteção.
- A estimativa de decaimento não decide se um material está apto ou inapto para uso clínico.

## Cálculo educativo
A função "Quanto sobra?" utiliza a relação:

`quantidade_restante = quantidade_inicial × (1/2) ^ (tempo_decorrido / meia_vida)`

As unidades de tempo precisam ser consistentes. Na base compartilhada do grupo, a meia-vida dos isótopos é armazenada em dias.
