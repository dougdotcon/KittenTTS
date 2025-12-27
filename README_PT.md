# KittenTTS 😻

**Um modelo de síntese de voz (TTS) ultra-leve e de alta qualidade, otimizado para CPU.**

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) [![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)

KittenTTS é um modelo de texto para voz (TTS) de código aberto com apenas 15 milhões de parâmetros. Projetado para implantação leve, ele oferece síntese de voz realista diretamente na CPU, tornando-o ideal para dispositivos de borda, desktops e aplicações web.

*Atualmente em Pré-visualização para Desenvolvedores*

[Entre no nosso Discord](https://discord.gg/upcyF5s6)

---

## ✨ Recursos

*   **Ultra-Leve:** O tamanho do modelo é inferior a 25MB, minimizando requisitos de armazenamento e largura de banda.
*   **Otimizado para CPU:** Executa-se eficientemente em CPUs padrão sem a necessidade de aceleração de hardware dedicada.
*   **Qualidade Premium:** Oferece um conjunto diversificado de vozes de alta fidelidade com entonação natural.
*   **Inferência Rápida:** Projetado para síntese de voz em tempo real com baixa latência.

---

## 🚀 Início Rápido

### Pré-requisitos

Certifique-se de ter o Python 3.8 ou superior instalado.

### Instalação

Instale o pacote mais recente diretamente dos lançamentos do GitHub:

bash
pip install https://github.com/KittenML/KittenTTS/releases/download/0.1/kittentts-0.1.0-py3-none-any.whl


### Uso Básico

Gere voz de alta qualidade com apenas algumas linhas de código:

python
from kittentts import KittenTTS
import soundfile as sf

# Inicializa o modelo
# O modelo é baixado automaticamente do Hub do Hugging Face
m = KittenTTS("KittenML/kitten-tts-nano-0.1")

# Gera o áudio
audio = m.generate(
    "Este modelo de TTS de alta qualidade funciona sem uma GPU",
    voice='expr-voice-2-f'
)

# Salva o resultado
sf.write('output.wav', audio, 24000)


### Vozes Disponíveis

O modelo suporta os seguintes presets de voz:

*   `expr-voice-2-m`
*   `expr-voice-2-f`
*   `expr-voice-3-m`
*   `expr-voice-3-f`
*   `expr-voice-4-m`
*   `expr-voice-4-f`
*   `expr-voice-5-m`
*   `expr-voice-5-f`

---

## 📦 Requisitos de Sistema

*   **SO:** Windows, macOS, Linux
*   **CPU:** Qualquer processador moderno x86 ou ARM
*   **Memória:** Uso mínimo de RAM, adequado para sistemas embarcados
*   **GPU:** Não requerida

---

## 🔮 Roadmap (Roteiro)

-   [x] **Lançamento de Visualização:** Modelo de pré-visualização para desenvolvedores lançado.
-   [ ] **Lançamento Completo:** Pesos de treinamento completos e documentação.
-   [ ] **SDK para Mobile:** Bibliotecas nativas para iOS e Android.
-   [ ] **Versão Web:** Implementação em navegador (WASM/WebGPU).

---

## 📄 Licença

Este projeto está licenciado sob a Licença Apache 2.0.
