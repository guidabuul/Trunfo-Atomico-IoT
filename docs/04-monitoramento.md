# 4. Monitoramento e alertas

O painel previsto pelo grupo reuniria as informações dos frascos identificados e as leituras dos sensores instalados no setor hospitalar. A aplicação registraria esses dados e apresentaria avisos quando identificasse alguma das situações definidas para o cenário.

## Movimentação dos frascos

O leitor RFID registraria a identificação de um frasco ao detectar sua etiqueta na porta do setor. A aplicação utilizaria esse registro junto às informações de movimentação cadastradas para verificar se houve uma saída e se ela estava autorizada.

Se o sistema identificasse uma saída sem autorização válida, o painel apresentaria um aviso. A leitura RFID, isoladamente, não informa a direção da passagem nem a localização contínua do frasco.

## Condições ambientais

O sensor Geiger-Müller permitiria acompanhar as leituras de radiação ambiental na sala de armazenamento. No cenário proposto, uma elevação em relação à condição definida para a demonstração poderia gerar um aviso no painel.

Os registros de temperatura e umidade também ficariam disponíveis para consulta. Essas informações ajudariam a acompanhar as condições do ambiente, sem que o grupo precise definir parâmetros operacionais de uma instalação hospitalar.

## Estimativa de decaimento

O Trunfo Atômico apresenta o conceito de meia-vida na função *Quanto sobra?*. A proposta de IoT aproveita esse mesmo cálculo para estimar a quantidade restante de uma fonte após determinado intervalo de tempo:

`Quantidade restante = Quantidade inicial × (1/2) ^ (Tempo decorrido / Meia-vida)`

Com a quantidade inicial, a meia-vida do isótopo e o tempo decorrido, o painel poderia mostrar a estimativa e indicar quando ela atingisse uma referência definida para o exercício. O tempo decorrido e a meia-vida precisam estar na mesma unidade.

Esse cálculo é teórico. Ele ajuda a relacionar o monitoramento ao conteúdo educativo do aplicativo, mas não substitui uma medição radiológica nem determina, por si só, se um material está adequado para uso.
