# 1. Contextualização da proposta

## Contexto do projeto

O Trunfo Atômico é um projeto educativo desenvolvido para o Challenge FIAP 2026, relacionado ao CTMSP e à Marinha do Brasil. O aplicativo apresenta isótopos e suas aplicações por meio de cartas, comparações de atributos e do cálculo de decaimento radioativo na função *Quanto sobra?*.

Para a disciplina de Disruptive Architectures: IoT, IoB & Generative IA, o grupo propõe estudar o uso de Internet das Coisas no acompanhamento de materiais radioativos em um setor hospitalar. A proposta se relaciona ao **Desafio 02 — Segurança física em instalações nucleares**, apresentado pela AMAZUL no kickoff do Challenge, em 13 de outubro de 2026.

## Problema abordado

No cenário considerado, é importante registrar a passagem de frascos por pontos de controle, acompanhar as condições do ambiente e consultar as informações de cada material. Reunir esses registros facilita a identificação de ocorrências e permite acompanhar, em um mesmo sistema, dados que teriam origens diferentes.

## Solução proposta

O grupo prevê uma etiqueta RFID em cada frasco e um leitor na porta do setor para registrar sua identificação. Um sensor Geiger-Müller acompanharia a radiação ambiental, enquanto outro sensor registraria temperatura e umidade. O ESP32 receberia essas informações e as enviaria por Wi-Fi, utilizando MQTT, para uma aplicação com armazenamento dos dados e painel de consulta.

Com esses registros, a aplicação poderia apresentar avisos sobre uma movimentação sem autorização e sobre alterações nas leituras de radiação ambiental. Também seria possível mostrar uma estimativa do decaimento de cada fonte, a partir dos dados de meia-vida.

## Relação com o Trunfo Atômico

O Trunfo Atômico trabalha o conceito de meia-vida de forma educativa. A proposta de IoT utiliza esse mesmo conhecimento em um exemplo de acompanhamento de materiais, mostrando como a identificação dos frascos e a coleta de dados poderiam apoiar o registro de eventos.

## Limites da proposta

A documentação descreve o funcionamento previsto, os componentes, a comunicação entre os dispositivos e o fluxo dos dados. O projeto não contempla, nesta etapa, a montagem de equipamentos, medições reais ou integração funcional com o aplicativo. Os exemplos de monitoramento e alerta são ilustrativos e não representam um sistema hospitalar em operação.
