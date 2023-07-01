journalctl -u starknetd -f
systemctl restart starknetd
wget -O starknet_update.sh https://api.nodes.guru/starknet_update.sh && chmod +x starknet_update.sh && ./starknet_update.sh

del node;
systemctl stop starknetd
systemctl disable starknetd
rm -rf ~/pathfinder/
rm -rf /etc/systemd/system/starknetd.service
rm -rf /usr/local/bin/pathfinder
