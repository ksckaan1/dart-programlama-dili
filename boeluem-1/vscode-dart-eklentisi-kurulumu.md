# VSCode Dart Eklentisi Kurulumu

Dart’ı indirdiğimize göre bize Dart kodlarımızı yazacağımız bir Tümleşik Geliştirme Ortamı \(IDE\) lazım. IDE’ler kodlarımızı yazarken kodların doğruluğunu kontrol eder ve kod yazarken önerilerde bulunur. Bu da kod yazarken işimizi kolaylaştırır.

Benim tavsiyem çoğu kodlama dilini yazarken kullandığım ve Dart yazanların da popüler olarak kullandığı **Visual Studio Code** programı.

Buradan İndirebilirsiniz

[https://code.visualstudio.com/Download](https://code.visualstudio.com/Download)

Linux İS kullananlara yine kullandıkları dağıtımın uygulama deposundan indirmelerini tavsiye ediyorum.

Visual Studio Code’dan ilerki zamanlarda **vscode** olarak bahsedeceğim.

Dart eklentisinin düzgün bir şekilde kurulabilmesi için bilgisayarımızda **git** komut-satırı uygulaması bulunması gerekir. Git’in yüklü olup olmadığını öğrenmek için komut satırına aşağıdakileri yazın:

`git --version`

Eğer versiyon numarasını gördüyseniz yüklü demektir. Eğer yüklü değilse veya git’i güncellemek istiyorsanız ki, mutlaka öneririm, aşağıda nasıl yükleneceğini görebilirsiniz.

Windows MacOS

Windows için: [Buradan İndirebilirsiniz](https://git-scm.com/download/win)

MacOS: [Buradan İndirebilirsiniz.](https://git-scm.com/download/mac)

**GNU/Linux İşletim Sistemleri**

**Debian/Ubuntu**

`sudo apt-get install git`

**Fedora**

`dnf install git`

**Arch Linux**

`sudo pacman -S git`

**Gentoo**

`emerge --ask --verbose dev-vcs/git`

**openSUSE**

`zypper install git`

**Mageia**

`urpmi git`

Git kurulumunu da yaptığımıza göre VSCode için Dart eklentisini kurabiliriz.

![VSCode Dart Eklentisi](../.gitbook/assets/dart-plugin.png)

Artık VSCode üzerinden Dart uygulaması geliştirebiliriz.

