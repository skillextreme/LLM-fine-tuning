# Fine-Tuning LLaMA 2 with QLoRA

This repository contains the code and documentation for fine-tuning the LLaMA 2 model using QLoRA (Quasi-hyperbolic Latent Residual Attention) parameters to enhance its performance on specific tasks. The fine-tuning process leverages the Hugging Face `transformers`, `datasets`, and `peft` libraries.

## Project Overview

The project aims to fine-tune the LLaMA 2-7b model to improve its understanding and generation capabilities. We use a dataset hosted on the Hugging Face Hub under the name `mlabonne/guanaco-llama2-1k` for training. This dataset provides targeted prompts to steer the model towards more specialized responses.

## Features

- **Model Loading with 4-bit precision**: Uses `BitsAndBytesConfig` for efficient model loading.
- **LoRA Adjustments**: Implements `LoraConfig` to inject trainable parameters without expanding the model size significantly.
- **Training Customization**: Uses `TrainingArguments` for detailed control over the training process, including precision, batch size, learning rate, and optimizer configuration.

## Installation

```bash
git clone https://github.com/<your-username>/llama2-finetune-qlora.git
cd llama2-finetune-qlora
pip install -r requirements.txt
