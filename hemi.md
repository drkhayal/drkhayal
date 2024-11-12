
# HEMI
![image](https://github.com/user-attachments/assets/c8b01d22-9fed-4fb5-beaa-5076a3e621e5)

### Discord : https://discord.gg/hemixyz

### Sistem istəkləri:
-------------------
### RAM : 2 GB
### Storage : 50 GB
### CPU : 2 Core

### Server update
```
sudo apt update
sudo apt install git make
```
###  Node running
```
cd
git clone https://github.com/hemilabs/heminetwork.git
cd heminetwork
make deps
make install
```
### Wallet creating
```
cd bin
./keygen -secp256k1 -json -net="testnet" > ~/popm-address.json

```
### Save wallet info
```
nano ~/popm-address.json
```
### Public hash bizim dc də faucetdən token istədiyimiz adresimiz. 
### Faucetdən tokenlərimizi alandan sonra ddavam edirik. 
### Servis fayl yaradırıq. Private key yazan yerə öz priv keyimizi yazmağı unutmuruq. !
```
sudo tee /etc/systemd/system/popmd.service <<EOF
[Unit]
Description=Popmd Service
After=network.target

[Service]
Type=simple
User=root
WorkingDirectory=/root/heminetwork
ExecStart=/root/heminetwork/bin/popmd
Environment="POPM_BTC_PRIVKEY=private yaz"
Environment="POPM_STATIC_FEE=50"
Environment="POPM_BFG_URL=wss://testnet.rpc.hemi.network/v1/ws/public"
Restart=always

[Install]
WantedBy=multi-user.target
EOF
```
### Lets run 
```
sudo systemctl daemon-reload
sudo systemctl enable popmd
sudo systemctl start popmd
```
### Check logs 
```
sudo journalctl -u popmd -fo cat
```
### Loglar belə görünürsə hər şey okaydir. 
![image](https://github.com/user-attachments/assets/556859a7-041b-4702-99d0-a04bff4a54de)
### Original guide: https://github.com/zeycan1/HEMI





