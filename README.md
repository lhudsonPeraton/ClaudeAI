# Demo: Run a Local LLM Coding Agent

1. Open VS Code.
2. Install llama.cpp, the software that will run the LLM. In a terminal, run:

   ```powershell
   irm https://llama.app/install.ps1 | iex
   ```

3. Start the server:

   ```powershell
   llama.exe serve
   ```

4. In another terminal, install an agent harness. We will install Pi:

   ```powershell
   irm https://pi.dev/install.ps1 | iex
   ```

5. Launch Pi:

   ```powershell
   pi
   ```

6. Now we can configure Pi to use our LLM:
   1. Run `/login llama.cpp`
   2. Press Enter twice.
   3. Run `/llama`
   4. Select **Download model**.
   5. Enter: `unsloth/gemma-4-E2B-it-GGUF:UD-IQ2_M`
      - If you have a gaming laptop you can try larger models if you have more VRAM:
        - [gemma-4-E2B-it-GGUF hardware compatibility](https://huggingface.co/unsloth/gemma-4-E2B-it-GGUF#:~:text=Hardware%20compatibility)
        - [Qwen3.8-27B-GGUF hardware compatibility](https://huggingface.co/unsloth/Qwen3.8-27B-GGUF#:~:text=Hardware%20compatibility)
   6. Press Enter again to load the model.
   7. Press Esc after the model finishes loading.
   8. Run `/model` and press Enter to select the model.
7. Ask about your codebase!
8. You can also try adding [packages](https://pi.dev/packages), for example:

   ```powershell
   pi install npm:pi-web-access
   ```
