<h1>ComfyUI Workflows</h1>

This folder contains some expanded workflows used to generate images with ComfyUI.
In their default use, the workflows allow the use of wildcards to create 4 different images for each prompt that can be reviewed and selected before finalizing generation. 

Each workflow has a set of groups and a note next to the group bypasser to explain the core features and usage.

# Ollama

Every workflow has the ability to use Ollama to convert SDXL-ready prompts into narrative ready prompts.

If Ollama is not available, simply bypass the group and populate the prompt manually.

Ollama might use VRAM that might be needed for the Image generations. Running Ollama on a separate machine might be a good option to release VRAM usage. Setting `keep alive` to `0` will unload the model immediately after the request finishes.

When using Ollama, we recommend the use of an instruction tuned model (the default in the workflow is `gpt-oss:20b`). Make sure to adapt the server URL (default is `http://ollama.internal:11434`) and the model name (default is `gpt-oss:20b`) to match your setup; clicking `Reconnect` will allow you to test the connection and list the available models.

Ollama-using workflows will convert the prompt using the system prompt present in the [ollama_sdxl2flux_qwen.txt](ollama_sdxl2flux_qwen.txt) file.

# SDXL, Illustrious and Pony

The [Smooth-SDXL_Illustrious-Ollama_txt2img-v3.1.json](Smooth-SDXL_Illustrious-Ollama_txt2img-v3.1.json) workflow is extended from the [Smooth Workflow (txt2img) v3.1](https://civitai.com/models/1598938/smooth-workflow-txt2img) workflow.

# Flux and Qwen

The [Atomix-Flux_Qwen-Ollama_txt2img-V4-SDXL_upscale.json](Atomix-Flux_Qwen-Ollama_txt2img-V4-SDXL_upscale.json) workflow is extended from the [Atomix FLUX txt2img Workflow v4.1](https://civitai.com/models/878828/atomix-flux-txt2img-workflow) workflow. 

# Z Image Turbo

The [Smith-ZImageTurbo-Ollama_txt2img-v4-SeedVR2.json](Smith-ZImageTurbo-Ollama_txt2img-v4-SeedVR2.json) workflow is extended from the [Z-Image Turbo - T2I Workflow + Detailer + SeedVR2 Upscaler + Color Grading v4.0](https://civitai.com/models/2174733?modelVersionId=2482034) workflow. 

# Work in progress

The [Gkr-SDXL_Pony_Illustrious-Ollama_txt2img-ViP.json](Gkr-SDXL_Pony_Illustrious-Ollama_txt2img-ViP.json) workflow is a Work-In-Progress combination, testing and tweaking of various elements from other workflows to generate an upscaled 16MP image as the final result while staying as close as possible to the original generation as generate CivitAI metadata for each stage of the image generation.

- Stage 1: Generate the regular image, pass it to a selector (can be bypassed for batch generation)
- Stage 2: Upscale to 4MP using HiResFix
- Stage 3: Use Ultimate SD Upscaler (No Upscale) to redefine the components of 4MP image using the original model and loras' specific characteristics. Faces and Eyes Detailer are then used on the resulting image.
- Stage 4: That result is sent to SeedVR2 to generate the final 16MP image.

There are many nodes involved in this workflow. Because of that I made use of multiple subgraphs to keep the workflow organized and easy to navigate.
Groups exists as organizational structure for the entire process and follow the Stage numbers.

It "works for me" but it might not be the best way to do it. Feedback is welcome.
