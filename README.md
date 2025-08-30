
```
sudo apt update
sudo apt install curl git jq lz4 snapd unzip bc -y
sudo apt upgrade -y
```
```
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | \
sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```
```
echo \
"deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] \
https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | \
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
docker --version
```
```
wget https://docs.linea.build/files/besu/besu-mainnet.zip
unzip besu-mainnet.zip
```
```
cd besu-mainnet
```
```
curl -Ls https://raw.githubusercontent.com/molla202/lina-mainnet-rpc-node/refs/heads/main/docker-compose.yaml > $HOME/besu-mainnet/docker-compose.yaml
curl -Ls https://raw.githubusercontent.com/molla202/lina-mainnet-rpc-node/refs/heads/main/config-snap-mainnet.toml > $HOME/besu-mainnet/config/config-snap-mainnet.toml
```
```
docker compose up -d
```
```
docker compose logs -f besu-mainnet
```
