<h1 align="center"> Aleo-Node-Kurulumu

  ## Root yetkisi almak için aşağğıdaki kodu giriyoruz bazı sunucularda bunu sürekli girmemiz gerekiyor. eğer bunu girmezseniz yazdığınız kodun başına sudo komutunu yazarkata devam edebilirsiniz ancak karışıklık olmaması için aşğıdaki komutu yazmanızı tavsiye ederim. ( root: Windows cihazlarda olduğu gibi yönetici olarak çalıştırmamıza, yani bize yetki veren bir komuttur.)
  ```
  sudo su
  cd
  ```
## Aşşağıdaki komutlarla sunucumuzdaki güncellemeleri, yükseltmeleri kontrol ediyoruz, sondaki -y işareti gelen onay işlemlerini otamatik olarak onaylanmasını sağlayacaktır. kısaca kurulum için sunucumuzu hazır hale getiriyoruz.


```
sudo apt update && sudo apt upgrade -y
```
```
 sudo apt install pkg-config curl git build-essential libssl-dev
 ```
 screen kur
```
sudo apt install screen -y
```
 Rust kuruyoruz.
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y
```
```
source $HOME/.cargo/env
```

Port ekleme
```
apt install ufw -y 
ufw allow ssh 
ufw allow https 
ufw allow http 
ufw allow 4133
ufw allow 3033
ufw enable
```


```

git clone https://github.com/AleoHQ/snarkOS.git --depth 1
```
```

cd snarkOS
```
```

./build_ubuntu.sh
```
```

cargo install --path .
```
```

screen -S client
```
```

./run-client.sh
```
```
snarkos account new
```
```

screen -S prover  ./run-prover.sh
```
