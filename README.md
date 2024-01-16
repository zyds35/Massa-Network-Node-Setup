# Massa-Network-Node-Setup

# Gereksinimler
8 cores, 16 GB RAM, 1TB disk

# Kurulum

> sudo apt update -y && sudo apt upgrade -y
> 
> ufw allow 31244 && ufw allow 31245
> 
> screen -S massa
> 
> wget https://github.com/massalabs/massa/releases/download/MAIN.2.0/massa_MAIN.2.0_release_linux.tar.gz
> 
> tar -zxvf massa_MAIN.2.0_release_linux.tar.gz
> 
> sudo apt install pkg-config curl git build-essential libssl-dev libclang-dev cmake
> 
> curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
> 
> source $HOME/.cargo/env

> rustup toolchain install 1.74.1
> rustup default 1.74.1
> rustc --version

> git clone https://github.com/massalabs/massa.git

> massa-node/config/config.toml
 [protocol]
 routable_ip = "ip adresinizi yazacaksınız buraya"
control x daha sonra y basıp enter diyoruz

> cd massa/massa-node/
> PASSWORD YAZAN YERE ŞİFRE BELİRLEYİP YAZIYORUZ
> ./massa-node -p <PASSWORD> |& tee logs.txt

> cd massa/massa-client/
> PASSWORD YAZAN YERE ŞİFRE BELİRLEYİP YAZIYORUZ
> ./massa-client -p <PASSWORD>
# Önemli Notlar
> log kontrolü için
> 
> screen -r massa
> 
> client içindeyken
> 
> cd massa/massa-client/
 ./massa-client
> private key'i SecretKey1 yazan yere yazıyoruz ve cüzdan adresimizi görüyoruz
 wallet_add_secret_keys SecretKey1
> roll almak için

> buy_rolls <address> <roll count> <fee>
> node_start_staking <your_address>
> get_addresses <your_address>

