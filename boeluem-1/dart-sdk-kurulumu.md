# Dart SDK Kurulumu

Dart SDK basit birkaç işlem ile işletim sisteminize kurabilirsiniz.

## Windows

Powershell'i Administratör olarak açalım ve aşağıdaki komutu girelim.

```text
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

Bu komut ile **Chocolately** paket yöneticisini kurmuş olduk. Test etmek için:

```text
choco -v
```

yazarak versiyon numarasını görebilirsiniz.  
Daha sonra buradan `dart-sdk` paketini yüklüyoruz.

```text
choco install dart-sdk
```

## GNU/Linux

### Debian Based \(Ubuntu, Linux Mint, ElementaryOS\)

Aşağıdaki komutları terminalde uyguluyoruz.

```text
sudo apt-get update
sudo apt-get install apt-transport-https
sudo sh -c 'wget -qO- https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add -'
sudo sh -c 'wget -qO- https://storage.googleapis.com/download.dartlang.org/linux/debian/dart_stable.list > /etc/apt/sources.list.d/dart_stable.list'
```

Sonra;

```text
sudo apt-get update
sudo apt-get install dart
```

### Arch Linux Based \(Manjaro\)

```text
sudo pacman -S dart
```

## MacOS

```text
brew tap dart-lang/dart
brew install dart
```

## Kontrol edelim:

```text
dart --version
```

