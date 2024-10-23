# Local AI Stack

This consists of a fairly comprehensive stack of AI tools that you can run locally for whatever you want.

Take note that this will use 4 GPUs as is. I think you'll need at least 2 for a decent experience and abiliyt to run LLMs and image models. I haven't tested with one GPU, but it may work. To adjust the number of GPUs, change the `device_ids` under `localai` and `comfyui`. Feel free to remove whatever you don't want to use.

## URL Reference

- localai: http://machine.ip.address.here:8080
- llm-proxy: http://machine.ip.address.here:3001
- open webui: http://machine.ip.address.here:3000
- searxng: http://machine.ip.address.here:8081
- comfy-ui: http://machine.ip.address.here:7860
- qdrant: http://machine.ip.address.here:6333
- n8n: http://machine.ip.address.here:5678

### LocalAI

Enables running open source LLMs/Transformers with support for distributed inferencing.

[LocalAI docs](https://localai.io/)

Thanks to [RoboTF AI](https://www.youtube.com/@RoboTFAI) who helped me get LocalAI working with distributed inferencing.

### LLM-Proxy

A simple proxy to make it easier to interact with local AI models. Aggregate models running on separate machines, adds TLS & api keys with the same method as OpenAI's API.

To set this up, refer to the [readme](https://github.com/j4ys0n/llm-proxy?tab=readme-ov-file).

### Open WebUI

A feature-rich UI for chatting with and interacting with your LLMs.
Open WebUI can use the following services in this stack. SearXNG, ComfyUI, LocalAI, or LocalAI with LLM-Proxy.

This tutorial helped me get ComfyUI running. [Techno Tim's Private AI Stack tutorial](https://technotim.live/posts/ai-stack-tutorial/)

[Open WebUI docs](https://docs.openwebui.com/)

### SearXNG

A privacy respecting, open source metasearch engine.

SearXNG uses the following services in this stack: Redis (Valkey)

[SearXNG docs](https://docs.searxng.org/)

### ComfyUI

A feature-rich and extensible Stable Diffusion UI, for generating and modifying images from prompt inputs. Works with Flux also.

### Qdrant

A vector database for the next generation of AI applications. Supports similarity search over any vector space and can be used to store arbitrary data like text, images etc.

### n8n

A highly extensible low-code automation and integration platform.

n8n uses the following services in this stack. Postgres, Qdrant, and LocalAI with LLM-Proxy.

[n8n docs](https://docs.n8n.io/)