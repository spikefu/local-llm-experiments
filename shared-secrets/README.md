# Can a local LLM write a functioning app in the form of a HTML file that uses public/private key pairs to allow two parties to securely share a message?

## Prompt
Write a single page HTML app that allows two parties to share information confidentially by allowing both parties to independently run the app locally. The app should allow the user to generate a public/private keypair with strong cryptography. The user can then share their public key via any channel of their choice. A user can then use a public key that has been shared with them to encrypt a payload that they paste into an appropriate input in the HTML app. The encrypted payload can then be shared via any channel of their choice and the receiver can use their private key (the pair of their public key) to decrypt the payload using appropriate input fields in the app. Save the file to shared-secrets-{model-name}.html

## Setup
**Claude Code CLI** version 2.1.138 invoked via Claude Code Router.

## Hardware
MacBook Pro M5 Max (18 Core CPU, 40 Core GPU, 16 Core Neural Engine), 128GB RAM.

## LLMs

### qwen3.6:35b-a3b-coding-bf16
Qwen struggles with this for some reason. It produces output that looks good, has appropriate error handling, but the app doesn't actually function.
Claude Code tried pretty hard to get things to work and sent the result back to the model for re-work 4 or 5 times.
In total it took about 21 minutes to finish the task and was close to maxing out the CPU most of the time.

You can see the terminal output in [qwen36-35b-a3b-coding-bf16.log](qwen36-35b-a3b-coding-bf16.log) and the HTML it produced in [shared-secrets-qwen36-35b-a3b-coding-bf16.html](shared-secrets-qwen36-35b-a3b-coding-bf16.html).

### gpt-oss:120b
I assume GPT is optimized for either this type of task or my hardware, or both. It completes the task in a little over 2 minutes and the app functions as requested. The final result is not as visually pleasing as the one Qwen produced, but there was nothing in the prompt asking for a pretty UI.

You can see the terminal output in [gpt-oss-120b.log](gpt-oss-120b.log) and the HTML it produced in [shared-secrets-gpt-oss-120b.html](shared-secrets-gpt-oss-120b.html).
