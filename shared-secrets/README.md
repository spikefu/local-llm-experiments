# Can a local LLM write a functioning app in the form of a HTML file that uses public/private key pairs to allow two parties to securely share a message?

## Prompt
See [prompt.md](prompt.md).

## Setup
Each run pairs a model with a runner/harness. Runners tried so far:

- **Ollama** via Claude Code CLI (through Claude Code Router)
- **Ollama** chat CLI (`ollama run`)
- **Ollama** GUI chat
- **Ollama** desktop app
- **LM Studio**
- **llama.cpp** CLI

## Hardware
MacBook Pro M5 Max (18 Core CPU, 40 Core GPU, 16 Core Neural Engine), 128GB RAM.

## Results

Each link below is a single-page HTML app produced by the model. Open it in a browser and try generating a keypair, encrypting a message, and decrypting it back — verdicts are left as an exercise for the reader.

### gpt-oss:120b

- Ollama + Claude Code — [html](gpt-oss-120b-olama-claude-code.html), [log](gpt-oss-120b-ollama-claude-code.log)
- Ollama chat CLI — [html](gpt-oss-120b-ollama-chat-cli.html)

### granite 4.1 30b

- LM Studio — [html](granite-41-30b-lmstudio.html)

### qwen3.5 35b-a3b

- Ollama GUI chat — [html](qwen35-35b-a3b-ollama-gui-chat.html)

### qwen3.6 35b-a3b

- Ollama chat CLI — [html](qwen36-35b-a3b-ollama-chat-cli.html)
- LM Studio — [html](qwen36-35b-a3b-lmstudio.html)
- llama.cpp CLI (q4_k_m) — [html](qwen3.6-35B-a3b-q4_k_m-llama-cpp-cli.html)
- llama.cpp CLI (q4_k_m, alt run) — [html](qwen36-35B-a3b-14_k_m-llama-cpp-cli.html)
- llama.cpp CLI (q8) — [html](qwen36-35b-a3b-q8-llama-cpp-cli.html)

### qwen3.6 35b-a23 (bf16)

- Ollama desktop app — [html](qwen36-35b-a23-bf16-ollama-app.html)

### qwen3.6 35b-a3b-coding (bf16)

- Ollama + Claude Code — [html](qwen36-35b-a3b-coding-bf16-ollama-claude-code.html), [log](qwen36-35b-a3b-coding-bf16-ollama-claude-code.log)
