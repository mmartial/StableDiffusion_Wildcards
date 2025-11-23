<h1>ComfyUI Workflows</h1>

This folder contains some slightly modified workflows used to generate images with ComfyUI.
The worklows make use of wildcards and will create 4 different images for each prompt that can be reviewed and selected before finalizing generation.

# Ollama

Some of the following workflows require a running instance of Ollama to convert SDXL-ready prompts into narrative ready prompts.

Ollama might use VRAM that you might need for the Flux/Qwen generations. If you have a way to run Ollama on a separate machine, this might be a good option to get better promots. 

When using Ollama, we recommend the use of an instruction tuned model (the default in the workflow is `gpt-oss:20b`). Make sure to adapt the server URL (default is `http://ollama.internal:11434`) and the model name (default is `gpt-oss:20b`) to match your setup; clicking `Reconnect` will allow you to test the connection and list the available models.

Ollama-using workflows will convert the prompt using the system prompt present in the [ollama_sdxl2flux_qwen.txt](ollama_sdxl2flux_qwen.txt) file.

# SDXL, Illustrious and Pony

The [SmoothWorkflowv3.1-mod.json](SmoothWorkflowv3.1-mod.json) workflow is based on the [Smooth Workflow (txt2img) v3.1](https://civitai.com/models/1598938/smooth-workflow-txt2img) workflow.

# Flux

The [AtomixFlux_txt2img_Workflow_V4-SDXLupscale.json](AtomixFlux_txt2img_Workflow_V4-SDXLupscale.json) workflow is based on the [Atomix FLUX txt2img Workflow v4.1](https://civitai.com/models/878828/atomix-flux-txt2img-workflow) workflow. 

## Flux with Ollama

Although SDXL-ready prompts can be used with Flux it is recommended to use the [AtomixFlux_Ollama_txt2img_WorkflowV4-SDXLupscale.json](AtomixFlux_Ollama_txt2img_WorkflowV4-SDXLupscale.json) workflow instead.

# Qwen

The [AtomixQwen_txt2img_WorkflowV4-SDXLupscale.json](AtomixQwen_txt2img_WorkflowV4-SDXLupscale.json) workflow is an adaptation of the previous Flux workflow to use Qwen instead.

# Qwen with Ollama

See [AtomixQwen_Ollama_txt2img_WorkflowV4-SDXLupscale.json](AtomixQwen_Ollama_txt2img_WorkflowV4-SDXLupscale.json).

