
### Farcaster Node Hubble

Guide Herculesden alınmadır. 
TG: https://t.me/HerculesNode

 * Rəsmi : https://docs.farcaster.xyz/hubble/hubble - https://www.thehubble.xyz/intro/hubble.html


## 🟢 Məlumat
- Bu guide ilə Farcaster nod qura bilərsiniz. 
- Bu nodu qura bilmək üçün  Warpcast hesabınızın olması lazımdır. Əgər yoxdursa burdan qeydiyyat ola bilərsiniz. Kart hesabından 5 usd çıxır. 9 manat civarı təxmini
Refli link: https://warpcast.com/~/invite-page/722705?id=32bdf721


## 🟢 Özəlliklər
- 16GB Ram istəyir. Amma az işlədir.  
- 4CPU
- 200 GB+
- Port 2281 - 2283 - Grafana üçün : 3000




## 🟢 Güncəlləmə
```shell
sudo apt update -y
```

```shell
sudo apt upgrade -y
```

```shell
apt install tmux
```

```shell
tmux new -s farcaster
```



## 🟢 Docker yükləyin	
- Docker qurulubsa `docker --version` yazıb kontrol edin. Əgər şəkildəki kimidirsə nəsə etməyə ehtiyac yoxdur. Deyilsə , qurun. 

![image](https://github.com/HerculesNode/Testnet-Rehber/assets/101635385/f7f9d70c-422b-4839-a8ad-e0daa12f4977)



```shell
sudo apt-get update
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
```
```shell
sudo mkdir -p /etc/apt/keyrings
```

```shell
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

```shell
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

```shell
sudo apt-get update
```

```shell
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

```shell
sudo systemctl start docker
sudo systemctl enable docker
```

```shell
sudo curl -L "https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

```shell
sudo chmod +x /usr/local/bin/docker-compose
```


## 🟢 Tək kod ilə qurulur

```shell
curl -sSL https://download.thehubble.xyz/bootstrap.sh | bash
```

- Burada sizdən ETH , OP mainnet ağında RPC istəyəcək.  
- Ala biləcəyiniz yerlər :  https://app.infura.io/dashboard və https://www.alchemy.com/  . İkisindən birini seçin. 

#### 1-ETH mainnet RPC linkini yazın
#### 2-Op Mainnet RPC linkini yazın
#### 3-Warpcast FID nömrənizi yazın. Profildə About yerində çıxır, olmasa profil adınızı yazın. 

![image](https://github.com/HerculesNode/Testnet-Rehber/assets/101635385/24432e01-c9c7-4a8c-b983-cf373f380082)



## 🟢 Son

- Aşağıdakı kimi cavab almalısınız.  Əvvəlcə snap yükləyəcək, bir az uzun çəkir , ondan sonra şəkildəki kimi bir ekran gələcək. 

![image](https://github.com/HerculesNode/Testnet-Rehber/assets/101635385/80611013-b51f-4c52-9fed-1284357d430f)

CTRL+B+D ilə tmuxdan çıxın. 


- Aşağıdakı kod ile FID  kontrol edə bilərsiniz. 

```shell
docker logs hubble-hubble-1 2>&1 | grep "Hub Operator FID"
```

![image](https://github.com/HerculesNode/Testnet-Rehber/assets/101635385/d0a4598e-b3a4-4ee3-a22b-5319f85c5c4f)


- Əlavə olaraq grafana ile kontrol edə bilərsiniz.  http://SERVER-IP:3000 

![image](https://github.com/HerculesNode/Testnet-Rehber/assets/101635385/1496c07d-c8b2-44ec-86ae-6b5fcada0526)


## 🟢 Əgər düzgün qurmusunuzsa bu fayllar görünməlidir. 

![image](https://github.com/HerculesNode/Testnet-Rehber/assets/101635385/cec5a452-e898-4801-a370-c39ea0bc96b1)




#### Sinxronizasiya olduğunu bilmək üçün grafana panelinizə baxın , aşağıdakı şəkildəki kimi 100% oldusa problem yoxdur. 

![image](https://github.com/HerculesNode/Testnet-Rehber/assets/101635385/dd393a7a-135a-4d2f-95be-f36ec884eb15)


