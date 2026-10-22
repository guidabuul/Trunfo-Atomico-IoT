# 1. Contextualização e proposta

## Contexto do trabalho

O Challenge 2026, realizado com o CTMSP/Marinha do Brasil, propõe aproximar a sociedade das aplicações da tecnologia nuclear. O grupo desenvolve o **Trunfo Atômico**, um aplicativo educativo com catálogo de isótopos, confronto de cartas por atributos e cálculo de decaimento radioativo. A versão 1.2.0 também prevê perguntas de "Mito ou verdade?" no detalhe das cartas.

Na disciplina de Disruptive Architectures: IoT, IoB & Generative IA, a contribuição do grupo consiste em estudar uma aplicação de Internet das Coisas associada ao tema. O recorte escolhido é o registro da movimentação de recipientes identificados e a observação de condições ambientais em um setor hospitalar que utiliza materiais radioativos.

A proposta dialoga com o **Desafio 02 — Segurança física em instalações nucleares**, apresentado pela AMAZUL no kickoff de 13/10/2026. Não se trata de instalar um sistema em hospital, mas de descrever seu funcionamento e representar seus dados em uma atividade educativa do Trunfo Atômico.

## Problema abordado

Em locais com materiais controlados, a identificação de recipientes, o registro de passagem e a observação de variáveis ambientais são atividades distintas. Sua integração em um único painel pode facilitar o acompanhamento de ocorrências e a compreensão dos dados produzidos pelos equipamentos.

## Objetivo

Apresentar uma arquitetura em que sensores e dispositivos de identificação enviam informações por rede a uma aplicação. O sistema registra os eventos e indica situações que merecem atenção, conforme regras definidas para a demonstração.

## Relação com o aplicativo

O jogo explica as características dos isótopos e a meia-vida. O módulo de IoT apresenta um exemplo de uso de sensores, identificação eletrônica e comunicação em rede. A função "Quanto sobra?" pode ilustrar uma estimativa teórica de decaimento, mas não substitui medições instrumentais.

## Delimitação da Sprint 1

O material é uma proposta conceitual. Não foram construídos equipamentos, executadas medições radiológicas ou implementada uma integração com o aplicativo. O modelo principal de dados do Trunfo Atômico permanece com AREA, FONTE, ISOTOPO e APLICACAO; eventuais registros de sensores pertencem a uma ampliação futura.

## Resultado da proposta

A documentação reúne os dispositivos previstos, a comunicação entre eles e as etapas de registro e consulta. O estudo será apresentado por meio da arquitetura e do fluxograma, conforme as exigências da Sprint 1.
