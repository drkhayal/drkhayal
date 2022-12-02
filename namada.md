# Namada Ceremony 

```
sudo apt update && sudo apt install -y curl git build-essential pkg-config libssl-dev
```

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y
```

```
source $HOME/.cargo/env
```
### Tmux açırıq. 
```
tmux new -s namada
```

```
git clone https://github.com/anoma/namada-trusted-setup.git && cd namada-trusted-setup && git checkout v1.1.0
```

```
cargo build --release --bin namada-ts --features cli
```
Bu hissə compiling çox uzun çəkə bilir. Komandı yazandan sonra tmuxdan çıxa bilərsiniz. (tmux+b sıxıb buraxdıqdan sonra D basmaqla)
```
mv target/release/namada-ts /usr/local/bin 
```
Daha sonra Maildə gələn vaxtınızın çatmağını gözləyin. Vaxtınız gələndə isə tmuxa daxil olub komandları yazın.
```
tmux a -t namada
```
Bu komandda token yerinə maildə sizə gələn keyi yazın.
```
namada-ts contribute default https://contribute.namada.net $TOKEN
```
