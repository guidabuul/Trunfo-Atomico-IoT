# 2. Equipamentos previstos

A definição abaixo descreve a função de cada componente na arquitetura. As especificações de interface e de instalação dependeriam da seleção dos módulos em uma etapa posterior.

| Componente | Função | Local previsto |
| --- | --- | --- |
| Etiqueta RFID | Identificar um recipiente por código | Identificação externa do recipiente |
| Leitor RFID | Registrar a passagem de uma etiqueta por um ponto | Acesso ao setor |
| ESP32 | Receber os dados dos módulos e encaminhar mensagens | Caixa de controle próxima aos dispositivos |
| Detector de radiação ambiental | Fornecer leituras do ambiente para a representação do sistema | Ponto de medição definido para a sala |
| Sensor de temperatura e umidade | Acompanhar condições ambientais | Sala de armazenamento |
| Ponto de acesso Wi-Fi | Disponibilizar conexão à rede | Infraestrutura local |
| Servidor com broker MQTT | Receber e distribuir mensagens | Infraestrutura lógica do sistema |
| Aplicação, armazenamento e painel | Registrar, consultar e apresentar os eventos | Sistema de informação |

## Identificação e leitura

O RFID realiza a identificação em pontos específicos. Uma passagem registrada no leitor não significa acompanhamento contínuo do recipiente. Tampouco informa, por si só, quem o transportou ou se houve autorização.

## Entradas do microcontrolador

As aulas abordam entradas digitais, leitura analógica e comunicação serial. A forma de conexão deve respeitar o funcionamento do módulo utilizado. Não é correto pressupor que todos os sensores serão lidos por uma entrada analógica. O ESP32 foi mantido por permitir comunicação Wi-Fi, necessária ao desenho proposto.

## Condições de uso

O detector radiológico indicado é apenas uma referência conceitual. Equipamentos utilizados em instalações reais precisam ser apropriados ao tipo de radiação, às condições de medição e às exigências de calibração e operação. Este trabalho não define especificações de radioproteção.
