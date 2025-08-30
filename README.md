



wget https://docs.linea.build/files/besu/besu-mainnet.zip
unzip besu-mainnet.zip

cd besu-mainnet

curl -Ls https://raw.githubusercontent.com/molla202/lina-mainnet-rpc-node/refs/heads/main/docker-compose.yaml > $HOME/besu-mainnet/docker-compose.yaml
curl -Ls https://raw.githubusercontent.com/molla202/lina-mainnet-rpc-node/refs/heads/main/config-snap-mainnet.toml > $HOME/besu-mainnet/config/config-snap-mainnet.toml

docker compose up -d
