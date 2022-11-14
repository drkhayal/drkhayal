# <h1 align="center"> Exorde </h1>


![image](https://user-images.githubusercontent.com/101149671/201298361-b48bc53b-7858-42c2-b6ab-5cf7270e3429.png)

<h1 align="center"> Salam, Coinlist tərəfindən yatırım almış proyekt olan ExordeLabs testnet guide.
</h1>

### Linkler:

 * [Telegram kanal](https://t.me/drtestnet)
 * [Exorde Discord Kanalı](https://discord.gg/RMHWfSypSv)
 * [Sıralama](https://explorer.exorde.network/leaderboard) və [Explorer](https://explorer.exorde.network/)
 * Telegram chat kanalımız [Telegram](https://t.me/drtestnetchat) 

## BƏzi qeydlər:

 * Bugün node quranlar Oktyabr 22'nə qədər %5 daha çox mükafat alacaq
 * Testnet fevral ayına qədər davam edəcək. 
 * Chain hələ də stabil deyil, ona görə də  "Please try restarting your application." kimi errorlar olarsa yenidən yoxlayın. 

## Sistem istəyi:
 (təxmini) 
``` 
CPU : 2 cores
RAM: 4Gb
SSD: 20Gb
```
## Docker ve güncəlləmələr::

```
sudo apt update -y && sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt install docker-ce
```

## Git clone 
```
git clone https://github.com/exorde-labs/ExordeModuleCLI.git
```

## Bura bir az uzun çəkə bilər:
```
sudo su
cd ExordeModuleCLI
docker build -t exorde-cli .
```

## Tmuxla yeni səhifə açırıq
```
tmux new -s exorde
```

## Metamask yazılan yerə 0x000-la başlayan adresinizi yazın.:

 * Testnet cüzdanı istifadə edin

```
docker run -it exorde-cli -m metamask -l 2
```

## və işləyirsə yazılar gedəcək. Tmuxdan ctrl+B basıb buraxan kimi D basıb çıxın. 


![image](https://user-images.githubusercontent.com/101149671/201302924-3d6c7127-6343-47fc-853b-353715b3e018.png)



## Tokenomicsə baxmaq istəsəniz:

![image](https://user-images.githubusercontent.com/101149671/201303557-755bcdc8-47f6-4a3e-a1a1-941e62342a37.png)





