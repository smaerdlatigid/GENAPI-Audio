# GENAI-Audio
Micro ML API for Audio Generation

## Set up

Build the docker image using cog:

`cog run -p 8090 bash`

## Example usage

Once in the docker container, run the gradio UI:

`python gradio_demo.py`

## Deploy locally

`cog predict -i prompt="Generate an energetic and bustling city street scene with distant traffic and close conversations"`

make sure to edit `predict.py` first to return a different response

`cog build -t genai-audio`

`docker run -d -p 5000:5000 --gpus 1 genai-audio`

`curl http://localhost:8188/predictions -X POST -H "Content-Type: application/json" -d '{"prompt": "futuristic race track in the sky"}'`

```python
import requests

response = requests.post(
    "http://localhost:5000/predictions",
    json={"prompt": "magical forest with birds chirping and a gentle breeze"}
)
print(response.json())
```