# Runnig GaGaNode on Linux VPS and Desktops
### Install Dependencies Packages
```bash
sudo apt-get update -y && sudo apt-get -y install curl tar ca-certificates
```

1.Download & Install
```bash
curl -o app-linux-amd64.tar.gz https://assets.coreservice.io/public/package/22/app/1.0.3/app-1_0_3.tar.gz && tar -zxf app-linux-amd64.tar.gz && rm -f app-linux-amd64.tar.gz && cd ./app-linux-amd64 && sudo ./app service install
```
2.Start Service
```bash
sudo ./app service start
```
3.Check APP Status
```bash
./app status
```

console output:

meson@meson-server:~/app-linux-amd64$ ./app status [gaganode]: local version:[1.0.3] latest version:[1.0.3] status:[DOWNLOADED]

4.Set Token
```bash
sudo ./apps/gaganode/gaganode config set --token=your_token_here
```
5.Restart APP
```bash
./app restart
```
