<h1>ComfyUI Workflows</h1>

This folder contains some expanded workflows used to generate images with ComfyUI.
In their default use, the workflows allow the use of wildcards to create 4 different images for each prompt that can be reviewed and selected before finalizing generation. 

Each workflow has a set of groups and a note next to the group bypasser to explain the core features and usage.

# Ollama

Every workflow has the ability to use Ollama to convert SDXL-ready prompts into narrative ready prompts.

If Ollama is not available, simply bypass the group and populate the prompt manually.

Ollama might use VRAM that might be needed for the Image generations. Running Ollama on a separate machine might be a good option to release VRAM usage.

When using Ollama, we recommend the use of an instruction tuned model (the default in the workflow is `gpt-oss:20b`). Make sure to adapt the server URL (default is `http://ollama.internal:11434`) and the model name (default is `gpt-oss:20b`) to match your setup; clicking `Reconnect` will allow you to test the connection and list the available models.

Ollama-using workflows will convert the prompt using the system prompt present in the [ollama_sdxl2flux_qwen.txt](ollama_sdxl2flux_qwen.txt) file.

# SDXL, Illustrious and Pony

The [Smooth-SDXL_Illustrious-Ollama_txt2img-v3.1.json](Smooth-SDXL_Illustrious-Ollama_txt2img-v3.1.json) workflow is extended from the [Smooth Workflow (txt2img) v3.1](https://civitai.com/models/1598938/smooth-workflow-txt2img) workflow.

# Flux and Qwen

The [Atomix-Flux_Qwen-Ollama_txt2img-V4-SDXL_upscale.json](Atomix-Flux_Qwen-Ollama_txt2img-V4-SDXL_upscale.json) workflow is extended from the [Atomix FLUX txt2img Workflow v4.1](https://civitai.com/models/878828/atomix-flux-txt2img-workflow) workflow. 

# Z Image Turbo

The [Smith-ZImageTurbo-Ollama_txt2img-v4-SeedVR2.json](Smith-ZImageTurbo-Ollama_txt2img-v4-SeedVR2.json) workflow is extended from the [Z-Image Turbo - T2I Workflow + Detailer + SeedVR2 Upscaler + Color Grading v4.0](https://civitai.com/models/2174733?modelVersionId=2482034) workflow. 
