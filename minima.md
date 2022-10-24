# Minima
## Ən ucuz serverə də qura bilərsiniz. Günə 1 token verir. 
1. Hər hansı bir server lazım olacaq. Məlumatlarını terminala yazıb girəcəksiniz. Proqram olaraq termius istifadə edirəm. 
2. https://incentive.minima.global/account/register?inviteCode=GDDABQGR - Bu sayta daxil olub qeydiyyatdan keçin. 
3. Terminala daxil olun və ardıcıl yazın. Tək script ilə qurulacaq.
```bash
wget -O minima_setup.sh https://raw.githubusercontent.com/minima-global/Minima/master/scripts/minima_setup.sh && chmod +x minima_setup.sh && sudo ./minima_setup.sh -r 9002 -p 9001
```

Qurulum bitdikdən sonra 2-3 dəqiqə gözləyin loglar axsın, sonra ctrl+c basıb logları dayandırın, xxx-ların yerinə minima saytında öz Incentive ID -nizi yazın.
```bash
curl 127.0.0.1:9005/incentivecash+uid:xxx-xxx-xxx-xxx-xxx
```
Daha sonra sayta qayıdıb refresh edin. Aşağıda son ping göstərəcək. Etdiyiniz həmin gün, həmin saat görünməlidir. Hər 24 saatda bir token gələcək. 

Telefona da qurula bilər, ancaq dəstəkləmədiyimdən onu paylaşmıram. 
Uğurlar. 

-----------------------------------------------------------------------
Bizi izləyin Telegram: https://t.me/drtestnet

Youtube: https://www.youtube.com/c/KhayalAll/videos

Twitter: https://twitter.com/xeyalall
