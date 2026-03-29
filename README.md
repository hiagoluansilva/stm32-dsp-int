# STM32 DSP Interrupt — ADC → Processamento → DAC

🇧🇷 **Português** | 🇺🇸 [English](#english)

---

## Português

Processamento digital de sinais em tempo real no STM32F4xx usando interrupção de ADC a 25 kHz, com saída via DAC.

### O que faz
- Amostra sinal analógico em **PA0** (ADC1 CH0) a **25 kHz** via interrupção
- Processa a amostra dentro do `ADC_IRQHandler`
- Gera saída processada em **PA4** (DAC CH1)
- TIM2 gera o trigger do ADC com precisão

### Configuração do Timer
```
TIM2: PSC = 839, ARR = 39
Frequência = 84 MHz / (840 × 40) = 2.500 Hz → 25 kHz de amostragem
```

### Mapa de pinos
| Pino | Função |
|---|---|
| PA0 | ADC1 CH0 — entrada analógica |
| PA4 | DAC CH1 — saída analógica |

### Microcontrolador
STM32F4xx — Atollic TrueSTUDIO

---

## English

Real-time DSP on STM32F4xx using ADC interrupt at 25 kHz, with DAC output.

### What it does
- Samples analog signal on **PA0** (ADC1 CH0) at **25 kHz** via interrupt
- Processes each sample inside `ADC_IRQHandler`
- Outputs processed signal on **PA4** (DAC CH1)
- TIM2 generates the precise ADC trigger

### Timer configuration
```
TIM2: PSC = 839, ARR = 39
Frequency = 84 MHz / (840 × 40) = 25 kHz sample rate
```

### Pin map
| Pin | Function |
|---|---|
| PA0 | ADC1 CH0 — analog input |
| PA4 | DAC CH1 — analog output |

### MCU
STM32F4xx — Atollic TrueSTUDIO
