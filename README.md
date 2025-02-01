# GENAI-Audio
Micro ML API for Audio Generation

## Set up

Build the docker image using cog:

`cog run -p 8090 bash`

## Example

Once in the docker container, run the gradio UI:

`python gradio_demo.py`

Navigate to [localhost:8090](http://localhost:8090) to see the UI.

## API

First, build the docker image using cog:

`cog build -t genai-audio`

Then, run the docker image:

`docker run -d -p 5000:5000 --gpus 1 genai-audio`

To check that the API is running, navigate to [localhost:5000](http://localhost:5000).

## Testing

