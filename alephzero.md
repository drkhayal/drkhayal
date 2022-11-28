# AlephZero-Testnet
## Sistem özəllikləri və mükafatlar haqqında informasiya. 
Mükafatlar hələ açıqlanmayıb, ancaq yaxın bir zamanda bununla bağlı məlumat verilməlidir. Blockchaindəki işləmləri təsdiq etdiyiniz müddət üçün ödəniş olunacağı deyilir.
![aleph zero sistem özəllikləri](https://user-images.githubusercontent.com/101218992/200110712-e6810440-73d6-49fc-8297-b83d5a8427f1.jpeg)
 
 ### Başa düşmədiyiniz yer olarsa, telegram kanalımızdan soruşa bilərsiniz. https://t.me/drtestnetchat

## 1)Güncəlləmə edirik
```
sudo apt update && sudo apt upgrade -y
```
## 2) Lazım olacaq komandaları yükləyirik 
```
sudo apt install wget git -y
```
```
sudo apt-get install docker.io -y
```
## 3)Aleph Node Runner faylını klonlayırıq.
```
git clone https://github.com/Cardinal-Cryptography/aleph-node-runner
cd aleph-node-runner
```
## 4)Nodumuzu işlədirik( nodeadı yazan yerə validator olaraq görünməsini istədiyiniz adı yazın) bu yükləmə uzun çəkə bilər, hər ehtimala tmuxun içində açın. 
```
./run_node.sh -n nodeadı --ip serveripadresi
```
## 5)Log görüntüləmə
```
docker logs --follow nodeadı
```
## 6)Validator üçün lazım olan məlumatları alırıq. Komanddan sonra çıxan məlumatları mütləq qeyd edin. 
```
./signer.sh
```
## 7) Cüzdan yaradırıq.  ( Cüzdanınız varsa elə onu istifadə edə bilərsiniz.) 
https://test.azero.dev/#/accounts səhifəsinə gedirik və 'add account' deyərək cüzdan yaradırıq.  
## 8)Validator üçün qeydiyyat edirik.
https://validators.alephzero.org/
Sayta daxil oluruq və mail adresimizi yazıb mailə gələn kodla təsdiq edib qeydiyyat edirik. Validator adı və sosial mediya hesablarımızı istəyir.Validator adı yerinə nodu quranda yazdığımız adı yazırıq. Digər məlumatları istədiyiniz kimi yazın. Bu məlumatlardan sonra  ' Become a Validator' yerində 'Apply' klik edirik.  5.  addımda yadda saxladığımız məlumatları burada yazırıq.  Stash account yerinə yeni açdığınız cüzdan adresini yazın. 
## 9)Təsdiqləmə işləmləri (bu təsdiqləmələri etməsəniz, validator olma istəyiniz rədd ediləcək ).
### Telemetry də Nod adınız görünəcək.(qurulum edərkən açıq olur, kontrol edə bilərsiniz.)
https://telemetry.azero.dev/#list/0x05d5279c52c484cc80396535a316add7d47b1c5b9e0398dd1f584149341460c5
### Kimlik Ayarı
https://test.azero.dev/#/accounts  Sayta daxil oluruq, cüzdanın sağ tərəfindəki üç nöqtəyə klik edib 'set on-chain identity' seçirik. Display name yerinə nod adımızı yazırıq, istəsəniz aşağıda olan məlumatları da doldura bilərsiniz.
![set on identity](https://user-images.githubusercontent.com/101218992/200088300-7e415edc-7871-4bc8-989f-8f304017ec3a.png)
### Faucet
https://faucet.test.azero.dev/ Günlük 25k token ala bilirsiniz. Burada 2 cüzdanla token alın, 2ci cüzdandan tokenləri əsas cüzdana yollayın. 
### Stash ve Bond 
https://test.azero.dev/#/staking/actions Açılan səhifədə sağ tərəfdə ' Stash' klik edirik və ən azı 25K token seçib , bond edirik.
### Session Key yaradırıq. (Çıxan məlumatı qeyd etməyi unutmayın!!)
Serverə bağlanıb aşağıdakı komandı yazırıq. 
```
curl -H "Content-Type: application/json" -d '{"id":1, "jsonrpc":"2.0", "method": "author_rotateKeys"}' http://127.0.0.1:9933
```

Çıxan yazı bu cür olacaq. ;
{"jsonrpc":"2.0","result":"0xa8bccfe29da88f256545d2addc194b734f615cec70b99845d56384e0c0c2fe64de211d8dd724dece2b3bc26c3250c550b644fb586c0875693ee1099c13feb806

Məlumatı qeyd edib saxlayın,  0x-ilə başlayan sizin session keyinizdi!
https://test.azero.dev/#/staking/actions   cüzdanımızın sağ tərəfində 'set session key'ə klik edərək , serverdən aldığımız keyi yazırıq və təsdiqləyirik. 
Təsdiqləndikdən sonra yenə eyni səhifədə sağ tərəfdə 'validate'ə klik edərək , fee yerinə 1-5 arası bir rəqəm yazıb, təsdiqləyirik. 
Bunları etdikdən sonra https://telemetry.azero.dev/#list/0x05d5279c52c484cc80396535a316add7d47b1c5b9e0398dd1f584149341460c5 saytında və https://test.azero.dev/#/staking saytında waiting yerində nod adımız görünəcək. 
#### Buraya  qədər olan addımları düzgün etmisinizsə, 1 həftə içində validatorunuz təsdiqlənəcək. 

### 0.8.0 Yenilənməsi
```
docker stop nodeadı 
cd aleph-node-runner
./run_node.sh -n nodeadı --ip serveripadresi 
cd
docker start nodeadı
```

