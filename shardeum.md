# Shardeum Betanet 1.1 Guide 
![image](https://user-images.githubusercontent.com/101635385/216447120-a1add722-5d7d-4403-b2a9-85ef054ba631.png)

 ## 🟢 Sistem tələbləri

* Proyekt tərəfindən istənilən  <br>
16 GB ram, 4+ GB <br>
60 GB ssd 



## 🟢 Sistemi Yeniləmə

Tmuxla yeni pəncərə açırıq. 

```shell
tmux new -s shardeum
```


```shell
sudo apt-get install curl
```

```shell
sudo apt update
```

## 🟢 1.Docker Qurulumu

```shell
sudo apt install docker.io
```

```shell
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

```shell
sudo chmod +x /usr/local/bin/docker-compose
```



## 🟢 2. İlk dəfə quracaq olanlar Cüzdan sıfırlama və köhnə cüzdanı silmə addımını etməsinlər

 <br> 


#### Metamask cüzdanımızı sıfırlayırıq.  Settings / General / Reset  <br><br> 

![image](https://user-images.githubusercontent.com/65338121/225295819-1be2ff9e-b5d9-4d6a-b916-d22a12f61313.png)
![image](https://user-images.githubusercontent.com/65338121/225296373-c4f30d57-b136-4071-8b7f-be6403d03520.png)
![image](https://user-images.githubusercontent.com/65338121/225296493-3420f3e3-2ec7-4f34-8515-b4adcb2c5aa2.png)

<br><br>

## 🟢  Daha öncəki nodu silirik.

```shell
cd ~/.shardeum
```

```shell
./cleanup.sh
```

```shell
cd ~/
```

```shell
rm -rf .shardeum
```

```shell
rm installer.sh
```


## 🟢 Yeni Nodu qururuq.


```shell
curl -O https://gitlab.com/shardeum/validator/dashboard/-/raw/main/installer.sh && chmod +x installer.sh && ./installer.sh
```


Aşağıdakı suallara cavab verin 

* By running this installer, you agree to allow the Shardeum team to collect this data. (y/n)?: y <br> 
 
* Do you want to run the web based Dashboard? (y/n): (y yazın) <br> 

* Set the password to access the Dashboard ( ŞİFRƏ YAZIN ) Bu Explorer üzərindən panelə bağlanma şifrəniz olacaq, unutmayın. <br> 

* Enter the port (1025-65536) to access the web based Dashboard (default 8080):  ( Enter basın və ya başqa port yazın, tövsiyyə olunan dəyişməməkdir. 8080 qalsın) <br> 

* This allows p2p communication between nodes. Enter the first port (1025-65536) for p2p communication (default 9001): Enter basın <br> 

* Enter the second port (1025-65536) for p2p communication (default 10001): Enter <br> 

* What base directory should the node use (defaults to ~/.shardeum): heçnə yazmayın, enter basın  <br> 


#### Lazım olanlar qurulacaq və sonunda aşağıdakı şəkil kimi görüntü olacaq.  <br> 

![image](https://user-images.githubusercontent.com/101635385/216449058-387d47b5-d6ef-423d-8501-4490f11c1c5f.png)


## 🟢 3. Təsdiqləyici

```shell
cd
```

```shell
cd .shardeum
```

```shell
./shell.sh
```

```shell
operator-cli gui start
```
  Son olaraq tmuxdan çıxmaq üçün ctrl+b+d edin. 
Artıq bundan sonrakı addımlar Explorer üzərindən olacaq


## 🟢 4. Explorer işləmləri.

https://NODIPADRESİNİZ:8080   ( chrome ya da hər hansı bir brauzerlər ip adresinizi yazaraq daxil olun. 

![image](https://user-images.githubusercontent.com/101635385/216449601-78112f06-5d93-41a2-a737-1826ee770529.png)

<br>


#### ilk olaraq Maintenance yerinə daxil oluruq.  Burada aşağıdakı şəkildə olan ağ butona basın və nodu işlətməyə başladın. Bir az gözləyin və səhifəni yeniləyin.  <br>


![image](https://user-images.githubusercontent.com/101635385/216450237-e595b7cd-97bc-4c13-843f-ec39586653a8.png)

![image](https://user-images.githubusercontent.com/101635385/216528434-df065848-606d-4bee-a1fd-cc07f9e80b42.png)




## 🟢 5. Cüzdan bağlamaq
1. Chainlist.org daxil olub cüzdanı qoşun. axtarış yerinə Sphinx yazın çıxacaq, cüzdana əlavə edin. Ya da əllə bir-bir aşağıdakı kimi edin.


2. Chain : Sphinx 1.X 

Aşağıdakı chaini Metamask cüzdanınıza əlavə edin.

Chain : Shardeum Sphinx 1.X <br>
New RPC URL : 	https://sphinx.shardeum.org/ <br>
Chain ID : 	8082 <br>
symbol : SHM <br>
Block Explorer URL :	https://explorer-sphinx.shardeum.org/ <br><br>


![image](https://user-images.githubusercontent.com/101635385/216532850-1c35b90f-d245-4be9-adf8-6c526d1c5ee3.png)





## 🟢 6. Faucet ve Stake etmə. 


1- Discorda daxil olun və  #faucet-1-1 kanalından SHM token ala bilərsiniz. 

 * [Discord FAUCET](https://discord.gg/shardeum)

![image](https://user-images.githubusercontent.com/101635385/219289164-5ce047bb-7a30-41d3-84a3-a40eaa2b5934.png)

![image](https://user-images.githubusercontent.com/101635385/216561514-37ab1ead-9801-421e-939b-459d93f9807b.png)



2 - [Twitter FAUCET](https://faucet-sphinx.shardeum.org/?_ga=2.223730200.2098418439.1675365683-1010477743.1666250200)

#### Faucetten tweet atın 15 SHM hesabınıza gələcək. 

![image](https://user-images.githubusercontent.com/101635385/216525966-93d207b1-910c-4dbe-a787-65a85439c99a.png)



#### Cüzdanınıza 15 SHM gəldikdən sonra ADD STAKE deyib 10 ədəd stake edin.   <br>


![image](https://user-images.githubusercontent.com/101635385/216532101-ca0e4aca-4422-42be-8241-51b723f92dc0.png)





## 🟢 7. Status kontrol etmə.

#### Stake işini edəndən sonra aşağıdakı kimi görünəcək, active yazısı görünmürsə səhifəni yeniləyin.


![image](https://user-images.githubusercontent.com/101635385/216527473-e8dc8f51-9b7d-4594-82b8-970ef71538c6.png)


## 🟢 Nominate key problemi həlli

![image](https://user-images.githubusercontent.com/101635385/219161856-c2ad942b-f923-4d1d-a5f7-d8f2f7966e47.png)


```shell
curl -O https://gitlab.com/shardeum/validator/dashboard/-/raw/main/installer.sh && chmod +x installer.sh && ./installer.sh
```





 ## 🟢 8080 port

Bu komanda  ilə 8080 portda işləyən başqa bir nodun olub-olmadığını yoxlayın. 

```shell
 lsof -i -P -n | grep LISTEN
```



 ## 🟢 ip 0.0.0.0 problemi olarsa həlli 

Bu komanda  ilə 8080 portda işləyən başqa bir nodun olub-olmadığını yoxlayın. 

```shell
cd ~/.shardeum
```

```shell
./shell.sh
```

Bu adresdən ip adresinizi öyrənin.

```shell
curl https://ipinfo.io/ip
```

Aşağıdakı komanda ilə ip adresinizi yazın.

```shell
operator-cli set external_ip IPADRESINIZ
```
Aşağıdakı komandaya nodu quranda yazdığınız external port məlumatını yazın. ( default 9001)
```shell
operator-cli set external_port PORTUNUZ
```
Gui'yi başladın.
```shell
operator-cli gui start
```
Ardından (https://NODEIPADRESINIZ:8080 (  chrome ya da hər hansı bir brauzerlər ip adresinizi yazaraq daxil olun) Səhifəyə daxil olub maintenance yerindən start edin .



## 🟢 Avtomatik nodu başlatma. 

Aşağıdakı kodu bir tmux  açaraq shardeum nodumuzun stoplama problemini həll edirik. 

```shell
tmux new -s shardeumstop
```

```shell
wget -q -O node_control.sh https://raw.githubusercontent.com/mesahin001/shardeum/main/node_control.sh && chmod +x node_control.sh && sudo /bin/bash node_control.sh
```

Nod guide üçün Herculesə təşəkkürlər :) 
linklərimiz: https://t.me/drtestnet
https://t.me/drtestnetchat



