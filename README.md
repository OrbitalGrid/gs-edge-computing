# gs-edge-computing
# OrbitalGrid — Sistema de Monitoramento de Satélites Solares

---

## Descrição do Projeto

O OrbitalGrid é um sistema de monitoramento de satélites equipados com painéis solares posicionados fora da órbita terrestre. O projeto simula um circuito de controle capaz de monitorar em tempo real a captação de energia solar e o risco de colisão com detritos espaciais, utilizando sensores conectados a um Arduino Uno e simulados no Wokwi.

---

## Objetivo da Solução

Captar energia solar fora da órbita terrestre, onde a incidência solar é contínua e sem interferências atmosféricas, maximizando a eficiência dos painéis solares. O circuito simula esse monitoramento por meio de um sensor de luminosidade (LDR) que representa os painéis solares, e um sensor ultrassônico que detecta a proximidade de detritos espaciais.

---

## Componentes Utilizados

| Componente                | Quantidade | Descrição                             |
|---------------------------|------------|---------------------------------------|
| Arduino Uno               | 1          | Microcontrolador principal            |
| LCD 16x2 I2C              | 1          | Display de informações em tempo real  |
| Sensor HC-SR04            | 1          | Sensor ultrassônico de distância      |
| Sensor LDR (Fotoresistor) | 1          | Sensor de luminosidade                |
| LED Verde                 | 1          | Indicador de risco baixo              |
| LED Amarelo               | 1          | Indicador de risco médio              |
| LED Vermelho              | 1          | Indicador de risco alto               |
| Buzzer                    | 1          | Alerta sonoro de colisão              |
| Resistores 1kΩ            | 3          | Proteção dos LEDs                     |
| Breadboard Half           | 1          | Protoboard para montagem              |

---

## Explicação do Funcionamento

O circuito realiza duas funções simultâneas exibidas no LCD 16x2:

### Captação de Energia Solar
O sensor LDR simula um painel solar. Quanto maior a luminosidade captada, maior o valor de energia exibido no display (0 a 100 KW), representando a captação de energia solar fora da órbita terrestre.

### Alerta de Colisão
O sensor ultrassônico HC-SR04 mede a distância de objetos próximos, simulando a detecção de detritos espaciais. O nível de risco é classificado em três categorias:

| Distância        | Nível de Risco | LED ativo | Buzzer              |
|------------------|----------------|-----------|---------------------|
| Acima de 25 cm   | BAIXO          | Verde     | Desligado           |
| Entre 10 e 25 cm | MEDIO          | Amarelo   | Tom grave (500 Hz)  |
| Abaixo de 10 cm  | ALTO           | Vermelho  | Tom agudo (1000 Hz) |

---

## Estrutura do Circuito

| Componente   | Pino Arduino |
|--------------|--------------|
| HC-SR04 TRIG | Pino 9       |
| HC-SR04 ECHO | Pino 8       |
| LED Verde    | Pino 13      |
| LED Amarelo  | Pino 12      |
| LED Vermelho | Pino 11      |
| Buzzer       | Pino 5       |
| LDR (AO)     | Pino A3      |
| LCD SDA      | Pino A4      |
| LCD SCL      | Pino A5      |

---

## Integrantes do Grupo

| Nome                        | RM     |
|-----------------------------|--------|
| Ana Beatriz Romão Pereira   | 571287 |
| Arthur Huang                | 571347 |
| Danilo Guerra               | 570617 |
| Gabriel Franchi             | 569668 |
| Nataly Brandino             | 573390 |

---
