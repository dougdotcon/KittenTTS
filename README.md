# KittenTTS 😻

**An ultra-lightweight, high-quality text-to-speech model optimized for CPU environments.**

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) [![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)

KittenTTS is an open-source text-to-speech model featuring just 15 million parameters. Designed for lightweight deployment, it delivers realistic voice synthesis directly on the CPU, making it ideal for edge devices, desktops, and web applications.

*Currently in Developer Preview*

[Join our Discord](https://discord.gg/upcyF5s6)

---

## ✨ Features

*   **Ultra-Lightweight:** Model size is less than 25MB, minimizing storage and bandwidth requirements.
*   **CPU-Optimized:** Runs efficiently on standard CPUs without the need for dedicated hardware acceleration.
*   **Premium Quality:** Offers a diverse set of high-fidelity voices with natural intonation.
*   **Fast Inference:** Engineered for real-time speech synthesis with low latency.

---

## 🚀 Quick Start

### Prerequisites

Ensure you have Python 3.8 or newer installed.

### Installation

Install the latest package directly from GitHub releases:

bash
pip install https://github.com/KittenML/KittenTTS/releases/download/0.1/kittentts-0.1.0-py3-none-any.whl


### Basic Usage

Generate high-quality speech with just a few lines of code:

python
from kittentts import KittenTTS
import soundfile as sf

# Initialize the model
# The model is automatically downloaded from the Hugging Face Hub
m = KittenTTS("KittenML/kitten-tts-nano-0.1")

# Generate audio
audio = m.generate(
    "This high quality TTS model works without a GPU",
    voice='expr-voice-2-f'
)

# Save the output
sf.write('output.wav', audio, 24000)


### Available Voices

The model supports the following voice presets:

*   `expr-voice-2-m`
*   `expr-voice-2-f`
*   `expr-voice-3-m`
*   `expr-voice-3-f`
*   `expr-voice-4-m`
*   `expr-voice-4-f`
*   `expr-voice-5-m`
*   `expr-voice-5-f`

---

## 📦 System Requirements

*   **OS:** Windows, macOS, Linux
*   **CPU:** Any modern x86 or ARM processor
*   **Memory:** Minimal RAM usage suitable for embedded systems
*   **GPU:** Not required

---

## 🔮 Roadmap

-   [x] **Preview Release:** Initial developer preview model released.
-   [ ] **Full Release:** Complete training weights and documentation.
-   [ ] **Mobile SDK:** Native libraries for iOS and Android.
-   [ ] **Web Version:** In-browser implementation (WASM/WebGPU).

---

## 📄 License

This project is licensed under the Apache 2.0 License.
