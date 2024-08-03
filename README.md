# Secure-Network-Connection
# < https://github.com/slackhq/nebula/releases >
1. sudo mkdir -p /usr/local/bin/snc && sudo mkdir /etc/snc
2. wget https://github.com/slackhq/nebula/releases/download/v1.9.3/nebula-linux-amd64.tar.gz
3. tar -xzf nebula-linux-amd64.tar.gz
4. sudo cp -r  nebula /usr/local/bin/snc/
6. sudo cp -r  nebula-cert /usr/local/bin/snc/
7. sudo cp -r  config.yml  /etc/snc/
8. cd /etc/snc/
9. sudo /usr/local/bin/snc/nebula-cert ca -name "Nebula CA"
11. sudo chmod 775 /etc/snc/ca.* 
13. sudo /usr/local/bin/snc/nebula-cert sign -name "host" -ip "172.52.0.1/8"
14. cp -r snc.service /etc/systemd/system/snc.service
15. systemctl start snc.service
