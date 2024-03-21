## Python version
Use python version 3.10.6
```
pyenv local 3.10.6
```


## To solve _lzma module not found error
[Best answer](https://stackoverflow.com/questions/59690698/modulenotfounderror-no-module-named-lzma-when-building-python-using-pyenv-on)
```
$  brew install xz
$  pyenv uninstall <desired-python-version>
$  pyenv install <desired-python-version>
```

## Fix python path
```
export PYTHONPATH=.
```

## Install missing dependencies
Donwload modules
```
pip download pytorch-lightning opencv-python imageio torchvision einops invisible-watermark omegaconf safetensors open_clip_torch kornia transformers git+https://github.com/openai/CLIP.git scipy -d dist/
```
Install modules
```
pip install dist/pytorch_lightning*.whl dist/opencv_python*.whl dist/imageio*.whl dist/torchvision*.whl dist/einops*.whl dist/imWatermark*.whl dist/invisible_watermark*.whl dist/omegaconf*.whl dist/safetensors*.whl dist/open_clip_torch*.whl dist/kornia*.whl dist/transformers*.whl dist/clip*.zip dist/scipy*.whl
```

pip download git+https://github.com/openai/CLIP.git -d dist/
pip download pytorch-lightning -d dist/
pip install dist/pytorch_lightning*.whl
export PYTHONPATH=.
pip download invisible-watermark -d dist/
pip install dist/opencv-python*.whl 
pip install dist/opencv_python-4.9.0.80-cp37-abi3-macosx_11_0_arm64.whl
pip download imageio -d dist/
pip install dist/imageio*.whl
pip download torchvision -d dist/
pip install dist/invisible_watermark*.whl
To solve _lzma error:

export PYTHONPATH=~/projetcs/core-harmony/generative-models.demo:$PYTHONPATH

pip install dist/imwatermark*.whl 

pip install dist/clip*.whl dist/safetensors*.whl 
pip install dist/open_clip_torch*.whl dist/kornia*.whl dist/transformers*.whl
pip download open_clip_torch kornia transformers -d dist/

pip download scipy -d dist/
pip install dist/scipy*.whl