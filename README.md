Here is a convenient source of models that can be downloaded: https://huggingface.co/TheBloke

For example, download 4-bit quantized WizardLM-7B from here: https://huggingface.co/TheBloke/wizardLM-7B-GGML/blob/main/wizardLM-7B.ggmlv3.q4_0.bin

Place it in the `models/` folder and run with

```bash
python3 -m llama_cpp.server --model models/wizardLM-7B.ggmlv3.q4_0.bin
```
