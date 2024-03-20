Original README click [here](url="https://github.com/elementlo/facechain/blob/main/README_ORI.md").

* Force to use the package diffusers v0.25.0 due to depracated code checked in 0.26.0.
* Make sure that "loss.requires_grad = True" is called in train_text_to_image_lora.py

# Installation
```
# Step1: use ModelScope or Colab with a GPU env.
# Note: at least 15GB of memory needs to be allocated.

# Step2: Entry the Notebook cell，clone FaceChain from github:
!GIT_LFS_SKIP_SMUDGE=1 git clone https://github.com/modelscope/facechain.git --depth 1

# Step3: Change the working directory to facechain, and install the dependencies:
import os
os.chdir('/mnt/workspace/facechain')    # You may change to your own path
print(os.getcwd())

!pip3 install gradio==3.50.2
!pip3 install controlnet_aux==0.0.6
!pip3 install python-slugify
!pip3 install onnxruntime==1.15.1
!pip3 install edge-tts
!pip3 install modelscope==1.10.0
!pip3 install diffusers==0.25.0

# Step4: Start the app service, click "public URL" or "local URL", upload your images to 
# train your own model and then generate your digital twin.
!python3 app.py
```
