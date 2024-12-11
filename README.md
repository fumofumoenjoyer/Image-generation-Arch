# Image-generation-Arch
Pytorch and huggingface setup for archlinux

Note Replace python-pytorch-cuda with whatever GPU you work with

```
yay -S python-huggingface-hub python-accelerate python-transformers python-diffusers python-pytorch-cuda
```


#python script
```
import torch  
from diffusers import DiffusionPipeline

pipe = DiffusionPipeline.from_pretrained("black-forest-labs/FLUX.1-dev")

prompt = "<<YOUR PROMPT>>"
image = pipe(prompt).images[0]
    
image.save("imagename.png")
```
