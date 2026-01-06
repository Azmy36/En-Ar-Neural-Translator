# 🌐 English to Arabic Neural Translator

This repository hosts a **Neural Machine Translation (NMT)** system designed to translate English text into Arabic.
It explores the evolution of NMT architectures, starting from a baseline **Seq2Seq LSTM** model and advancing to an **Attention-Based** model for improved accuracy and long-sentence handling.

> **⚠️ Important:**
> The project expects a parallel corpus (English-Arabic) dataset. In the notebooks, data is loaded from a specific path (e.g., Google Drive), which may need adjustment for your local environment.

## 📌 Features

- **Sequence-to-Sequence (Seq2Seq)**: Implements the Encoder-Decoder paradigm for text generation.
- **Attention Mechanism**: Allows the decoder to focus on relevant parts of the source sentence at each generation step, solving the bottleneck issue of fixed-length vectors.
- **Bilingual Support**: Specifically optimized for English → Arabic translation tasks.
- **Framework**: Built using **TensorFlow/Keras**.

## 🧠 Model Architectures

### **1. Baseline Model (`NMT_Baseline.ipynb`)**
- **Encoder**: LSTM layers processing the English input.
- **Context Vector**: The final hidden state of the encoder passed to the decoder.
- **Decoder**: LSTM layers generating the Arabic translation token by token.

### **2. Attention Model (`NMT_With_Attention.ipynb`)**
- **Bahdanau / Luong Attention**: Computes context vectors dynamically for every time step.
- **Impact**: Significantly better performance on longer sentences compared to the baseline.

## 📂 Repository Structure

```
.
├── NMT_Baseline.ipynb        # Baseline Seq2Seq LSTM implementation
├── NMT_With_Attention.ipynb  # Advanced model with Attention Mechanism
└── README.md                 # Project documentation
```

## 📊 Dataset

**Format**: Tab-separated text file (`eng \t arabic`).
**Preprocessing**: The notebooks include steps for cleaning Arabic text (normalization) and English text, as well as tokenization and padding.

## ⚙️ Installation & Usage

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/Azmy36/En-Ar-Neural-Translator.git
    cd En-Ar-Neural-Translator
    ```

2.  **Install dependencies**:
    ```bash
    pip install tensorflow numpy scikit-learn
    ```

3.  **Run the Notebooks**:
    - Start with `NMT_Baseline.ipynb` to understand the core concepts.
    - Move to `NMT_With_Attention.ipynb` to see the performance improvements.

## 👨‍💻 Author

**Youssef Mohamed Moussa**
- 📧 Email: [youssefazmy36@gmail.com](mailto:youssefazmy36@gmail.com)
