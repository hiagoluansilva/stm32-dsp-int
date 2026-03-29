# stm32-dsp-int

Processamento Digital de Sinais com ADC, DAC e interrupções no STM32F4xx.

## Descrição

Projeto de DSP em tempo real que realiza aquisição via ADC, processamento do sinal e saída via DAC, sincronizados por timer e utilizando interrupções para garantir taxas de amostragem precisas.

## Periféricos utilizados

| Periférico | Função |
|------------|--------|
| ADC1 | Aquisição do sinal de entrada |
| DAC | Saída do sinal processado |
| TIM2 | Trigger de amostragem |
| USART2 | Debug / comunicação serial |

## Estrutura

```
DSP_Int/
├── Src/
│   ├── main.c
│   ├── stm32f4xx_it.c   # Handlers de interrupção
│   └── system_stm32f4xx.c
├── Inc/
└── Drivers/
```

## IDE

Atollic TrueSTUDIO 9.3 / STM32CubeIDE

## Escola

Centro Tecnológico Liberato — Novo Hamburgo/RS
