## Conda Environment Setup
```console
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm ~/miniconda3/miniconda.sh
```

After installing, close and reopen your terminal application or refresh it by running the following command:

```console
source ~/miniconda3/bin/activate
conda init --all
```

## Create Environment:

```console
conda create -n erwan python=3.10
conda activate erwan
```

```console
conda create -n erwan python=3.10
conda activate erwan
```

## To Run Jupyter Notebook 

```console
pip install notebook
```

---
```console
sudo apt-get install wget gpg
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -D -o root -g root -m 644 packages.microsoft.gpg /etc/apt/keyrings/packages.microsoft.gpg
echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" |sudo tee /etc/apt/sources.list.d/vscode.list > /dev/null
rm -f packages.microsoft.gpg
```

```console
sudo apt install apt-transport-https
sudo apt update
sudo apt install code # or code-insiders
```
---

Make sure to install the python and jupyter extensions in vs code, just go to the extentions tab.

Select the Kernel after this.

## Install packages

```console
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu
pip install scikit-learn scipy tqdm pillow matplotlib scikit-image pandas
```

## Github

Check First if it's already installed

```console
git version
```

If not, install it:

```console
sudo apt-get update
sudo apt-get install git-all
```

**Clone**

```console
git clone https://github.com/samyuktsriram/ens100.git
git config user.email "sriramsamyukt@gmail.com"
git config --global user.name "samyuktsriram"
```

Activate Conda Environment

```console
conda activate /mnt/disks/location/conda/envs/shared_env
```















