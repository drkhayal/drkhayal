# Aleo Snarkos nod qurulumu

### Scripti işə salırıq. 

```
wget -q -O aleo_snarkos3.sh https://github.com/drkhayal/drtestnetann/blob/main/aleo_snarkos3.sh && chmod +x aleo_snarkos3.sh && sudo /bin/bash aleo_snarkos3.sh
```
### Aleo akkauntunuzun məlumatlarına baxmaq üçün. Burda çıxacaq məlumatları bir yerə qeyd edin
```
cat $HOME/aleo/account_new.txt
```
### Hansı private key olduğuna baxmaq üçün 
```
grep "prover" /etc/systemd/system/aleo-prover.service | awk '{print $5}'
```
### Loglara baxmaq üçün
```
journalctl -u aleo-prover -f -o cat
```
### Clientin loglarına baxmaq üçün
```
journalctl -u aleo-client -f -o cat
```
### Aleo Proveri saxlamaq və clienti başlatmaq
```
systemctl stop aleo-prover
systemctl restart aleo-client
```
### Proveri başlatmaq. 
```
systemctl stop aleo-client
systemctl restart aleo-prover
```
### Snarkosu silmək üçün
```
wget -q -O aleo_remove_snarkos.sh https://api.nodes.guru/aleo_remove_snarkos2.sh && chmod +x aleo_remove_snarkos.sh && sudo /bin/bash aleo_remove_snarkos.sh
```
