# Sonaric AI Node 
![image](https://pbs.twimg.com/media/GO0Ojjga4AAqFnm?format=jpg&name=4096x4096)

Minimum Sistem istəyi :
✅ 4 GB RAM
✅ 2 CPU cores
✅ 20 GB free disk space
✅ 64-bit operating system

### linklər
[Explorer](https://tracker.sonaric.xyz/)   /
[Twitter](https://x.com/Sonaricnetwork)    /
[Discord](https://discord.gg/fs7XnKbTWw) 

## 🟢 Portlar : 
![image](https://github.com/aksamlan/Sonaric/blob/main/portlar.png?raw=true)

## 🟢 Sistemi güncəlləmək
```shell
sudo apt update && \
sudo apt install curl git jq build-essential gcc unzip wget lz4 -y
```

## 🟢 Lazım olan faylları yükləyib, icazələri veririk. 
```shell
wget https://raw.githubusercontent.com/aksamlan/Sonaric/main/sonaric.sh && chmod +x sonaric.sh && ./sonaric.sh
```


## 🟢 Nodun düzgün qurulub , qurulmadığını kontrol edirik 
```shell
sonaric node-info
```

## 🟢 GUI'yi başladın.
➖ Öz  terminalinizi açın
➖ "user@your-vps-ip" öz IP'nizlə dəyişdirin (məsələn: root@123.456.789)
```shell
ssh -L 127.0.0.1:44003:127.0.0.1:44003 -L 127.0.0.1:44004:127.0.0.1:44004 -L 127.0.0.1:44005:127.0.0.1:44005 -L 127.0.0.1:44006:127.0.0.1:44006 user@your-vps-ip
```


## 🟢 Severdəki məlumatları yaddaşda saxlayın. 
```shell
sonaric identity-export -o mysonaric.identity
```
## 🟢 Serverdə pointlərinizi görmək üçün bu kodu yazın. 
```shell
sonaric points
```
## 🟢 Ad dəyişdirmək üçün bu kodu yazın və sonra adınızı yazın. 
```shell
sonaric node-rename
```

mysonaric.identity faylını kompunuzda uyğun bir yerdə yaddaşda saxlayın. 

Original Guide:  - https://github.com/aksamlan/Sonaric
