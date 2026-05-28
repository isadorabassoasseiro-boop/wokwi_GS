# 🌱 OrbitGuard

## 📖 Descrição do Projeto

O **OrbitGuard** é uma solução tecnológica desenvolvida para auxiliar no monitoramento climático agrícola. O sistema utiliza sensores conectados ao Arduino para coletar dados ambientais em tempo real, permitindo a análise de riscos relacionados às mudanças climáticas que podem afetar plantações.

A proposta do projeto é simular um sistema inteligente inspirado em tecnologias de monitoramento via satélite, realizando análises de:

- temperatura;
- umidade;
- quantidade de chuva.

Com base nesses dados, o sistema identifica níveis de risco agrícola e apresenta os resultados visualmente por meio de LEDs e display LCD.

Além disso, esta simulação em Arduino funciona como uma etapa de coleta de dados ambientais para o sistema desenvolvido em Python. As informações capturadas pelo Arduino são utilizadas posteriormente no projeto em Python para realizar análises de desastres naturais agrícolas, classificação de riscos climáticos e geração de recomendações preventivas.

---

# 🎯 Objetivo da Solução

O principal objetivo da solução é auxiliar produtores rurais no monitoramento climático da plantação, permitindo identificar possíveis riscos agrícolas como:

- 🌡️ seca agrícola;
- 🌧️ excesso de chuva;
- ☀️ calor extremo;
- 💧 estresse hídrico;
- 🌊 encharcamento do solo.

Além disso, o sistema busca apresentar essas informações de forma visual, intuitiva e acessível.

---

# 🛠️ Componentes Utilizados

| Componente | Função |
|---|---|
| Arduino Uno R3 | Controlador principal do sistema |
| Sensor DHT11 | Leitura de temperatura e umidade |
| Potenciômetro | Simulação da intensidade da chuva |
| LCD 16x2 I2C | Exibição das informações |
| LED Verde | Indicação de risco baixo |
| LED Amarelo | Indicação de risco moderado |
| LED Vermelho | Indicação de risco alto/crítico |
| Resistores 220Ω | Proteção dos LEDs |
| Breadboard | Organização das conexões |
| Jumpers | Realização das conexões elétricas |

---

# ⚙️ Explicação do Funcionamento

## 🌡️ Temperatura e Umidade

O sensor **DHT11** realiza a leitura da:

- temperatura ambiente;
- umidade do ar.

Esses dados são enviados ao Arduino para análise.

---

## 🌧️ Simulação da Chuva

A intensidade da chuva é simulada utilizando um **potenciômetro** conectado à entrada analógica `A0` do Arduino.

O sistema converte os valores analógicos em porcentagem de chuva simulada.

---

## 📡 Integração com o Sistema em Python

O Arduino atua como uma etapa de monitoramento climático responsável pela coleta dos dados ambientais da plantação.

As informações coletadas pelo circuito:

- temperatura;
- umidade;
- intensidade da chuva;

são utilizadas no sistema desenvolvido em Python para realizar:

- análise climática;
- classificação de risco;
- identificação de possíveis desastres naturais agrícolas;
- geração de recomendações preventivas.

Dessa forma, o Arduino funciona como uma simulação de sensores ambientais conectados a uma central inteligente de monitoramento agrícola.

---

## 📊 Análise Climática

Com base nos dados coletados, o sistema classifica:

- temperatura;
- umidade;
- chuva.

Após isso, é calculado o nível de risco climático.

| Situação | Risco |
|---|---|
| Condições estáveis | 🟢 Baixo |
| Pequenas alterações climáticas | 🟡 Moderado |
| Situações perigosas | 🔴 Alto |
| Situações extremas | 🚨 Crítico |

---

# 💡 LEDs Indicadores

Os LEDs representam visualmente o risco climático identificado pelo sistema.

| LED | Significado |
|---|---|
| 🟢 Verde | Risco baixo |
| 🟡 Amarelo | Risco moderado |
| 🔴 Vermelho | Risco alto/crítico |

---

# 🖥️ Display LCD

O display LCD apresenta:

- temperatura;
- umidade;
- chuva simulada;
- risco climático.

## Exemplo de exibição:

```text
T:30C U:45%
C:60% R:Moderado
```

---

# 🔌 Estrutura do Circuito

## 📍 Sensor DHT11

| DHT11 | Arduino |
|---|---|
| VCC | 5V |
| GND | GND |
| DATA | D2 |

---

## 📍 Potenciômetro

| Potenciômetro | Arduino |
|---|---|
| Pino esquerdo | GND |
| Pino central | A0 |
| Pino direito | 5V |

---

## 📍 LEDs

| LED | Arduino |
|---|---|
| LED Verde | D8 |
| LED Amarelo | D9 |
| LED Vermelho | D10 |

Todos os LEDs utilizam resistores de `220Ω`.

---

## 📍 LCD I2C

| LCD I2C | Arduino |
|---|---|
| VCC | 5V |
| GND | GND |
| SDA | A4 |
| SCL | A5 |

---

# ▶️ Instruções de Execução

## 🚀 Executando no Wokwi

1. Abrir o simulador Wokwi;
2. Criar um novo projeto com Arduino Uno;
3. Adicionar os componentes utilizados;
4. Realizar as conexões do circuito;
5. Inserir o código do projeto;
6. Adicionar as bibliotecas necessárias;
7. Executar a simulação.

---

# 📚 Bibliotecas Necessárias

Adicionar as seguintes bibliotecas:

```txt
DHT sensor library
Adafruit Unified Sensor
LiquidCrystal I2C
```

---

# 🧪 Como Testar o Sistema

## 🌡️ Alterando temperatura e umidade

Clique sobre o sensor **DHT11** e altere os valores manualmente.

---

## 🌧️ Simulando chuva

Gire o potenciômetro para simular:

- chuva baixa;
- chuva moderada;
- chuva alta.

---

# ✅ Resultado Esperado

O sistema deverá:

- 📟 exibir os dados no LCD;
- 📊 mostrar o risco climático;
- 💡 acender os LEDs conforme o risco identificado;
- 📡 simular a coleta de dados ambientais utilizados pelo sistema em Python.

---

# 👨‍💻 Tecnologias Utilizadas

- Arduino C/C++;
- Wokwi Simulator;
- Python;
- Sensores DHT11;
- LCD I2C;
- Componentes eletrônicos básicos.

---

# 🌍 Finalidade do Projeto

O projeto foi desenvolvido com foco em soluções tecnológicas para agricultura inteligente, buscando reduzir impactos causados por mudanças climáticas e auxiliar no monitoramento preventivo de riscos agrícolas.
