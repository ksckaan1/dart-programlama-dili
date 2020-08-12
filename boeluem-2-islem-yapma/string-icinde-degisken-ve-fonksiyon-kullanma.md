# String İçinde Değişken ve Fonksiyon Kullanma

Bu işlemi `${}` ile yapabiliriz. İşte örneğimiz;

```dart
int carp(int a, b) {
  return a * b;
}

main() {
  print("3 X 5 = ${carp(3, 5)}");
}
```

Yukarıda gördüğümüz gibi `print` fonksiyonu içerisine **`${`**`carp(3, 5)`**`}`** ekleyerek `carp` fonksiyonundan dönen sonucu `string`'e eklemesini sağladık.

Bunu aynı şekilde değişkenler için de kullanabiliriz.

```dart
main() {
  String isim = "Kaan";
  print("Merhaba ${isim}!");
}
```

