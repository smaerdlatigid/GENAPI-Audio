# GENAI-Audio
Micro ML API for Audio Generation

Model Details: https://github.com/hkchengrex/MMAudio

## Set up

Build the docker image using cog:

`cog run -p 8090 bash`

## Example

Once in the docker container, run the gradio UI:

`python gradio_demo.py`

Navigate to [localhost:8090](http://localhost:8090) to see the UI.

### To Do
- Create predict.py for inference endpoint
- Play with text prompt vs. static image vs. equirectangular crop + pan video
- save weights to current directory