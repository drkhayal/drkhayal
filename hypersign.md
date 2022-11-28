# Hypersign Nod qurulumu
## Sistem istəkləri 
### Minimum
* 3x CPU; 
* 4GB RAM
* 80GB Disk
* Qalıcı internet bağlantısı (testnet sırasında trafik minimum 10Mbps olacaq )
 
### Məsləhət görülən 
* 4x CPU;
* 8GB RAM
* 200 GB depolama (SSD və ya NVME)
* Qalıcı internet bağlantısı (testnet sırasında trafik minimum 10Mbps olacaq )
### Tək script ilə avtomatik qurulum üçün 
```
wget -O hype.sh https://raw.githubusercontent.com/drkhayal/hypersign/main/hype.sh  && chmod +x hype.sh && ./hype.sh
```
### Sinxron olmağı yoxlamaq üçün.
```
hid-noded status 2>&1 | jq .SyncInfo
```
### Cüzdan yaratma
```
hid-noded keys add cüzdanadı
```
Cüzdan recover etmək üçün 
```
hid-noded keys add cüzdanadı --recover
```
Mövcud cüzdanlara baxmaq üçün 
```
hid-noded keys list
```
### Discorda daxil olub faucetdən token istəyin. 
https://discord.gg/Jxg4mewh

### Validator yaratmaq. 
```
hid-noded tx staking create-validator \
  --amount 1999000uhid \
  --from cüzdanadı \
  --commission-max-change-rate "0.01" \
  --commission-max-rate "0.2" \
  --commission-rate "0.07" \
  --min-self-delegation "1" \
  --pubkey  $(hid-noded tendermint show-validator) \
  --moniker nodeadı \
  --chain-id jagrat \
  --fees 250uhid
```
