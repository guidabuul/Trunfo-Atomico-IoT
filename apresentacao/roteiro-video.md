# Roteiro de apresentação — cerca de 5 minutos

Este roteiro é uma referência para a gravação. A apresentação deve mostrar o fluxograma e explicar o percurso das informações.

## 0:00–0:40 | Contexto
Apresentar o Trunfo Atômico, o desafio educativo sobre tecnologia nuclear e as três funcionalidades do aplicativo: Álbum, Duelo e "Quanto sobra?".

## 0:40–1:25 | Relação com a AMAZUL
Explicar o Desafio 02, ligado à segurança física em instalações nucleares. Apresentar o monitoramento hospitalar como exemplo conceitual e o laboratório virtual como extensão educativa do jogo.

## 1:25–2:20 | Componentes
Explicar etiqueta e leitor RFID, sensor ambiental de radiação, sensor de temperatura e umidade e ESP32. Indicar onde cada componente estaria instalado e o que registraria.

## 2:20–3:20 | Comunicação
Mostrar o diagrama: sensores e RFID → ESP32 → Wi-Fi → broker MQTT → aplicação → registro e painel. Explicar que o broker recebe e distribui mensagens, enquanto a aplicação interpreta os eventos.

## 3:20–4:20 | Fluxograma e alertas
Percorrer uma leitura na saída do setor. A aplicação consulta a autorização; se não houver registro válido, gera um alerta educativo. Mencionar os avisos ambientais simulados e a diferença entre medição e estimativa por meia-vida.

## 4:20–5:00 | Benefícios e encerramento
Retomar o objetivo educativo: aproximar conhecimentos de IoT, redes e tecnologia nuclear. Reforçar que a Sprint 1 apresenta uma proposta conceitual, sem implantação hospitalar.

## Conferência antes de publicar
- [ ] Mostrar o fluxograma com legibilidade.
- [ ] Explicar sensores, comunicação e uso dos dados.
- [ ] Citar o Desafio 02 da AMAZUL.
- [ ] Distinguir simulação educativa de monitoramento real.
- [ ] Publicar no YouTube como **não listado**.
- [ ] Adicionar o link do vídeo ao README e à entrega da disciplina.
