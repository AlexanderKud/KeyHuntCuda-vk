# KeyHuntCuda - vk

--------------------------------------------------------------------------------------------------------------------




#Tutorial: Instalação e Uso do Código

Cuda 12.6
````
sudo su
wget https://developer.download.nvidia.com/compute/cuda/repos/wsl-ubuntu/x86_64/cuda-wsl-ubuntu.pin
sudo mv cuda-wsl-ubuntu.pin /etc/apt/preferences.d/cuda-repository-pin-600
wget https://developer.download.nvidia.com/compute/cuda/12.6.2/local_installers/cuda-repo-wsl-ubuntu-12-6-local_12.6.2-1_amd64.deb
sudo dpkg -i cuda-repo-wsl-ubuntu-12-6-local_12.6.2-1_amd64.deb
sudo cp /var/cuda-repo-wsl-ubuntu-12-6-local/cuda-*-keyring.gpg /usr/share/keyrings/
sudo apt-get update
sudo apt-get -y install cuda-toolkit-12-6
````
Install libgm
````
apt install -y libgmp-dev
````
Python 
````
sudo apt-get install python3.9
````
Clonar o repositório
````
git clone https://github.com/vkThiago/KeyHuntCuda-vk.git
````
Instalação sem placa de video
````
cd KeyHuntCuda-vk
make all
````
Instalação com placa de video
````
cd KeyHuntCuda-vk
make gpu=1 CCAP=86 all
````

O CCAP deve ser de acordo com a sua placa, segue abaixo uma lista com os principais modelos e o seu CCAP relativo.

Arquitetura Ampere (mais recente para desktops e data centers):
NVIDIA RTX 4090 – Compute Capability: 8.9
NVIDIA RTX 4080 – Compute Capability: 8.9
NVIDIA RTX 4070 Ti – Compute Capability: 8.9
NVIDIA RTX 4060 – Compute Capability: 8.9
NVIDIA A100 – Compute Capability: 8.0
NVIDIA A40 – Compute Capability: 8.6
NVIDIA A30 – Compute Capability: 8.0
NVIDIA A10 – Compute Capability: 8.6
NVIDIA A100 Tensor Core – Compute Capability: 8.0
Arquitetura Turing:
NVIDIA RTX 3090 – Compute Capability: 8.6
NVIDIA RTX 3080 – Compute Capability: 8.6
NVIDIA RTX 3070 – Compute Capability: 8.6
NVIDIA RTX 2080 Ti – Compute Capability: 7.5
NVIDIA RTX 2080 Super – Compute Capability: 7.5
NVIDIA RTX 2070 Super – Compute Capability: 7.5
NVIDIA RTX 2060 Super – Compute Capability: 7.5
NVIDIA TITAN RTX – Compute Capability: 7.5
Arquitetura Volta:
NVIDIA Titan V – Compute Capability: 7.0
NVIDIA V100 Tensor Core – Compute Capability: 7.0
Arquitetura Pascal:
NVIDIA GTX 1080 Ti – Compute Capability: 6.1
NVIDIA GTX 1080 – Compute Capability: 6.1
NVIDIA GTX 1070 – Compute Capability: 6.1
NVIDIA Tesla P100 – Compute Capability: 6.0
NVIDIA GTX Titan X (Pascal) – Compute Capability: 6.1

----------------------------------------------------------------------------------------------------------------------------------