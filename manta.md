# Manta Trusted Setup Ceremony node qurulumu. 

## Formu doldurduqdan sonra mail gələndən sonra bunu edin. 

### Yenilənmə edirik. 
```
sudo apt update
```
### Lazım olan komandları yükləyirik. 
```
sudo apt install pkg-config build-essential libssl-dev curl jq
```
### Rust yükləyirik. 
```
curl https://sh.rustup.rs/ -sSf | sh -s -- -y
```
### Mənbəni göstəririk.  
```
source $HOME/.cargo/env
```
### Faylları yükləyirik.  
```
git clone https://github.com/Manta-Network/manta-rs.git
```
### Tmux açırıq
```
tmux new -s manta
```
### Contribution kodunu yazırıq. 
```
cargo run --release --all-features --bin groth16_phase2_client contribute
```
### Qurulum tamamlandıqdan sonra çıxan nəticəni tvit olaraq paylaşın. 
Daha sonra tmuxdan ctrl+b sıxıb, buraxan kimi D klik edib tmuxdan çıxırıq. 
