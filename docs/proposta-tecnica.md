# Proposta técnica

## Contexto
O Trunfo Atômico é um aplicativo educativo que apresenta isótopos e suas aplicações por meio de cartas, duelo de atributos e cálculo de meia-vida. A proposta de IoT amplia a abordagem didática para um exemplo de monitoramento de materiais radioativos em ambiente hospitalar.

A aplicação se relaciona ao Desafio 02 — Segurança física em instalações nucleares, apresentado pela AMAZUL no kickoff do Challenge em 13/10/2026. O exemplo hospitalar é um cenário didático de local que utiliza ou armazena materiais radioativos.

## Problema e necessidade
Em um cenário de controle de materiais, é necessário identificar passagens de recipientes por pontos definidos, acompanhar condições do ambiente e registrar eventos que mereçam verificação. A coleta automática pode reduzir a dependência de registros manuais e facilitar a visualização de ocorrências.

## Aplicação de IoT
O sistema previsto utiliza etiquetas RFID nos recipientes, leitor de passagem, sensores de radiação ambiental e de temperatura/umidade, além de um ESP32. Os registros são enviados pela rede a uma aplicação que alimenta um painel educativo.

Não se propõe rastreamento de localização contínuo: cada leitura RFID indica apenas a detecção no ponto onde o leitor está instalado.

## Integração com o Trunfo Atômico
O álbum e o duelo ensinam sobre isótopos; a função "Quanto sobra?" calcula uma estimativa teórica de decaimento. Na extensão IoT, o estudante pode observar eventos de identificação e condições ambientais, compreendendo a distinção entre dados de sensores e cálculos físicos.

O recurso "Mito ou verdade?" pertence ao Álbum na versão 1.2.0 e não altera os componentes de IoT desta Sprint.

## Resultado esperado
- Exibir identificação e horário de passagem de um recipiente em um ponto monitorado.
- Apresentar temperatura, umidade e leitura ambiental simuladas.
- Sinalizar uma saída sem autorização registrada.
- Ilustrar uma condição ambiental fora dos parâmetros estabelecidos no cenário.
- Apresentar uma estimativa de decaimento, sem tratá-la como medição.

## Limites do escopo
A Sprint 1 é exclusivamente conceitual: não há construção, calibração de equipamentos ou validação em ambiente clínico. Uma solução real dependeria de planejamento técnico, instrumentos apropriados, procedimentos de radioproteção e avaliação de profissionais habilitados.
