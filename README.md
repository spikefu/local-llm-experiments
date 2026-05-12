# local-llm-experiments

A collection of experiments exploring what local LLMs can do — running models on consumer hardware.

Each experiment lives in its own directory with a README describing the prompt, the models tried, and observations about the results.

## Hardware

MacBook Pro M5 Max (18 Core CPU, 40 Core GPU, 16 Core Neural Engine), 128GB RAM.

## Experiments

- [shared-secrets](shared-secrets/) — Can a local LLM build a single-page HTML app that uses public/private keypairs to let two parties exchange encrypted messages? Compares several models across a few local runners (Ollama, LM Studio, llama.cpp).
