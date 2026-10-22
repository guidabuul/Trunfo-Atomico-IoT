# 4. Registro de eventos e monitoramento

O acompanhamento proposto reúne identificação de recipientes e informações do ambiente. Cada dado deve ser interpretado segundo sua origem e finalidade.

| Evento | Tratamento previsto | Informação apresentada |
| --- | --- | --- |
| Identificação de etiqueta na saída | Consultar se há autorização válida para a movimentação | Registro de saída ou aviso de ocorrência |
| Leitura ambiental | Comparar o valor com parâmetro definido apenas para a demonstração | Registro da leitura e indicação de atenção |
| Temperatura e umidade | Apresentar valores e verificar faixa definida no cenário | Histórico e aviso didático |
| Consulta de um isótopo | Aplicar a fórmula de decaimento aos dados informados | Quantidade restante estimada |

## Exemplo de passagem sem autorização

Quando uma etiqueta é lida na saída, a aplicação registra o evento. Em seguida, procura uma autorização vinculada à movimentação. Caso não encontre uma autorização válida, apresenta um aviso no painel. A consulta à autorização é uma etapa independente da leitura RFID.

## Estimativa da meia-vida

A funcionalidade educativa "Quanto sobra?" utiliza a expressão:

`quantidade restante = quantidade inicial × (1/2) ^ (tempo decorrido / meia-vida)`

Na base de dados compartilhada do grupo, a meia-vida está expressa em dias. As unidades de tempo utilizadas no cálculo devem ser compatíveis.

O resultado é uma estimativa matemática de decaimento. Não equivale a um laudo, medição radiológica ou decisão de aptidão para uso clínico.

## Limites da proposta

Os alertas aqui descritos são exemplos didáticos. Não foram definidos limiares clínicos, critérios de proteção radiológica ou procedimentos de resposta a ocorrências reais. Essas definições não integram a atividade.
