# Step-by-step: run local models with GGML (~5min + download time for model weights)

### Setup Python environment

1. Clone this repository `git clone https://github.com/continuedev/ggml-server-example`
2. Move into the folder: `cd ggml-server-example`
3. Create a virtual environment: `python3 -m venv env`
4. Activate the virtual environment: `source env/bin/activate` on Mac, `env\Scripts\activate.bat` on Windows, `source env/bin/activate.fish` if using fish terminal
5. Install required packages: `pip install -r requirements.txt`

### Download a model

6. Download a model to the `models/` folder
   - Here is a convenient source of models that can be downloaded: https://huggingface.co/TheBloke
   - For example, download 4-bit quantized WizardLM-7B from here: https://huggingface.co/TheBloke/wizardLM-7B-GGML/blob/main/wizardLM-7B.ggmlv3.q4_0.bin

### Serve the model

7. Run the server with `python3 -m llama_cpp.server --model models/wizardLM-7B.ggmlv3.q4_0.bin`

### Use with Continue

8. To set this as your default model in Continue, you can open `~/.continue/config.json` either manually or using the `/config` slash command in Continue. Then, set `"default_model": "ggml"`, reload your VS Code window, and you're good to go!

---

## Any questions?

Happy to help. Email use at hi@continue.dev.
