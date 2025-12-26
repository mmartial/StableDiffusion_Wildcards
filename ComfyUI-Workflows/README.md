<h1>ComfyUI "Combined Workflow"</h1>

_(Looking for the older workflows? You can find them in the [Older](Older) folder)_

This folder contains a "Combined Workflow" (nearly 500KB)that does SDXL, Pony, Illustrious, Flux1D, Qwen and ZImageTurbo generation with an optional prompt extension using Ollama and Wildcards processing.

The workflow contains a "READ ME FIRST" section that details some about how it came to be, what it does and how to use it. Please refer to it for more information.

FYSA: list of used custom nodes:
```bash
❯ fgrep cnr_id gkr-combined_v1.json| tr -s " " | sort | cut -d ":" -f 2 | uniq
 "cg-image-filter",
 "comfy-core",
 "comfy-image-saver",
 "ComfyLiterals",
 "ComfyMath",
 "ComfyUI_ADV_CLIP_emb",
 "ComfyUI_Comfyroll_CustomNodes",
 "comfyui_ultimatesdupscale",
 "comfyui-art-venture",
 "comfyui-custom-scripts",
 "comfyui-easy-use",
 "comfyui-fbcnn",
 "comfyui-image-saver",
 "comfyui-impact-pack",
 "comfyui-impact-subpack",
 "comfyui-inspire-pack",
 "comfyui-kjnodes",
 "comfyui-logicutils",
 "comfyui-lora-manager",
 "comfyui-ollama",
 "controlaltai-nodes",
 "rgthree-comfy",
 "seedvr2_videoupscaler",
 ```