# Secure-Network-Connection
# <<<<<<<<< https://github.com/slackhq/nebula/releases >>>>>>>>
1. wget https://github.com/slackhq/nebula/releases/download/v1.9.3/nebula-linux-amd64.tar.gz
2. tar -xzf nebula-linux-amd64.tar.gz
3. sudo cp -r  nebula /usr/local/bin/snc/
4. sudo cp -r  nebula-cert /usr/local/bin/snc/
5. sudo cp -r  snc /etc/
6. sudo /usr/local/bin/snc/nebula-cert ca -name "Nebula CA"
7. sudo mv  ca.* /etc/snc/
8. sudo chmod 775 /etc/snc/ca.* 
9. cd /etc/snc/
10.sudo /usr/local/bin/snc/nebula-cert sign -name "host" -ip "192.0.2.6/8"
11.cp -r snc.service /etc/systemd/system/snc.service
12.systemctl start snc.service
