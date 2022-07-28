# Trinton-Deployment


## Serve a Model in 3 Easy Steps

### Step 1: Create the example model repository 
TBD

### Step 2: Launch triton from the NGC Triton container
```
# use one gpu resources
sudo docker run --gpus=1 --rm --net=host -v /PAHT/model_repository:/models  -it nvcr.io/nvidia/tritonserver:22.06-py3 bash

pip install numpy pillow transformers==4.18.0
pip3 install torch torchvision torchaudio
tritonserver --model-repository=/models
```

### Step 3: In a separate console, launch the image_client example from the NGC Triton SDK container

TBD