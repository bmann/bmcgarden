---
draft: "true"
---
Downloaded [[Pinokio]] and installed [[ComfyUI]], it includes the ability to install Stable Diffusion and Stable Video within it. Can't quite get SD running?

Used Pinokio to install [[Open WebUI]].

Open WebUI wants [[Ollama]] installed, so over to manually install Ollama. The [[Caret]] plugin also wants Ollama as the local option.

> [!Instructions from Caret plugin settings]
> Remember to do the following:
> 
> Make sure you have downloaded the model you want to use:
> 
> `ollama run llama3`
> 
> After running the model, kill that command and close the ollama app.
> 
> Then run this command to start the Ollama server and make it accessible from Obsidian:
> 
> `OLLAMA_ORIGINS=app://obsidian.md* ollama serve`

Tried out some chats and put them in [[Canadian Elevator Startup]]

Caret has a subfolder in the Obsidian vault, that has the chats inside it. I'm going to commit this to git, but I'm going to exclude it from being generated as part of the Jekyll build process.