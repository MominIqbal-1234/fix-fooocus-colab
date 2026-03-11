```
%cd /content

!pip uninstall -y torch torchvision torchaudio
!pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121

!git clone https://github.com/lllyasviel/Fooocus.git || true

%cd /content/Fooocus

!pip install -r requirements_versions.txt

!pip uninstall -y numpy cupy cupy-cuda12x cupy-cuda11x
!pip install "numpy<2" cupy-cuda12x pygit2==1.15.1

!python launch.py --share --always-high-vram
```
