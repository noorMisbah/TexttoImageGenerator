# TexttoImageGenerator
Text to image generation using hugging face
#install diffusers
!pip install diffusers transformers

#using stable diffusion here
from diffusers import StableDiffusionPipeline
import matplotlib.pyplot as plt
import torch

#model from hugging face
model_id="sd-legacy/stable-diffusion-v1-5"

#using stable diffusion and running on GPU
pipe=StableDiffusionPipeline.from_pretrained(model_id,torch_dtype=torch.float16)
pipe=pipe.to("cuda")

#for giving prompt
prompt="girl riding a horse in a sunny weather"

#To display image
plt.imshow(images)
