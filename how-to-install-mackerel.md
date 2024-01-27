How to install Mackerel (Cách cài đặt Mackerel)

wget -q -O - https://mackerel.io/file/script/setup-all-apt-v2.sh | MACKEREL_APIKEY='<YOUR_API_KEY>' sh
sudo apt-get update
sudo apt-get install mackerel-agent
sudo systemctl start mackerel-agent
sudo journalctl -u mackerel-agent.service
