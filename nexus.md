# Nexus

> Nexus üçün kontrakt deploy edib, faylı yadda saxlayırıq. 

> İstənilən serverdə etmək olar.  



![image](https://github.com/ruesandora/Nexus/assets/101149671/9fcbe5d7-d88c-49b8-af65-768132f75176)


# Node qurulumu 

```console
# update etmək
sudo apt update -y && sudo apt upgrade -y
sudo apt install cmake
sudo apt install build-essential
```

#

```console
# rustup qurmaq

# 1 cini seçin
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

# rust bitdikdən sonra
. "$HOME/.cargo/env"
rustup target add riscv32i-unknown-none-elf
```

#

```console
# nexus tool qurmaq

# bura uzun çəkir, errorlara fikir verməyin .
cargo install --git https://github.com/nexus-xyz/nexus-zkvm nexus-tools --tag 'v1.0.0'

# nexus yaradırıq.
cargo nexus new nexus-project

# main.rs dəyişdiririk
cd nexus-project
```

#

```console

# bu fayla giririk.
nano ./src/main.rs
# içindəki kodları silib aşağıdakı kodu yazın. 
```

```console
#![no_std]
#![no_main]

fn fib(n: u32) -> u32 {
    match n {
        0 => 0,
        1 => 1,
        _ => fib(n - 1) + fib(n - 2),
    }
}

#[nexus_rt::main]
fn main() {
    let n = 7;
    let result = fib(n);
    assert_eq!(result, 13);
}
```

#

```console
# kontrakt run edin. 
cargo nexus run
cargo nexus run -v

# prove olmasını gözləyin 
cargo nexus prove

# verify işini tamamlayın. 
cargo nexus verify
```

#

> Burdakı  `nexus-proof` file özünüzdə saxlayın. 

<img width="417" alt="Ekran Resmi 2024-06-14 11 02 40" src="https://github.com/ruesandora/Nexus/assets/101149671/b6468869-3274-4b05-857d-a82263729585">

