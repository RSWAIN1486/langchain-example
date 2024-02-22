# Examples to use Langchain Agents on CPU

# Pre-Requisites
## Setup EC2 32 cores

```bash
sudo apt install zip python3-pip
curl -fsSL <https://get.docker.com> -o get-docker.sh
sudo usermod -aG docker $USER
pip install jupyterlab
echo "export PATH=\\$PATH:/home/ubuntu/.local/bin" >> ~/.bashrc
```

## Start a local Jupyter lab and Setup Local AI with Langchain

```bash
jupyter lab --ip 0.0.0.0
pip install localai langchain
```

### Clone this repo
```bash
git clone https://github.com/RSWAIN1486/langchain-example.git
cd langchain/
```

### Download the Mixtral model and move it to models folder
```bash
wget https://huggingface.co/TheBloke/Mixtral-8x7B-Instruct-v0.1-GGUF/resolve/main/mixtral-8x7b-instruct-v0.1.Q3_K_M.gguf
mv mixtral-8x7b-instruct-v0.1.Q3_K_M.gguf models/
```

### Start the server and start executing the langchain notebook
```bash
docker compose up -d
```

### View its logs
```bash
docker compose logs -f
```
