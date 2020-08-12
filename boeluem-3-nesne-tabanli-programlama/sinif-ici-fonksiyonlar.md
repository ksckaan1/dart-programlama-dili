# Sınıf-içi Fonksiyonlar

Bir önceki konuda sınıf oluştururken insan üzerinden örnek vermiştik. Yine aynı örnek üzerinden gidelim.

{% page-ref page="siniflar.md" %}

`insan` sınıfımıza bir özellik _\(yani fonksiyon\)_ ekleyelim. Bu özelliği tıpkı gerçek bir insanda bulunan kendini tanıtabilme yeteneği olsun.

```dart
class insan {
  String isim;
  int yas;
  double kilo;

  insan({String isim = "Kaan", int yas = 23, double kilo = 78.2}) {
    this.isim = isim;
    this.yas = yas;
    this.kilo = kilo;
  }

  void kendiniTanit() {
    print("Merhaba, Ben " + this.isim);
  }
}

main() {
  insan kisi1 = new insan(isim: "Erkay", kilo: 78.2);
  kisi1.kendiniTanit(); //Merhaba, Ben Erkay
}
```

`insan` sınıfımızın içerisine `kendiniTanit` adında bir fonksiyon ekledik. Fonksiyonumuz bir değer döndürmediği için tipini `void` yaptık. `print` fonksiyonu ile ekrana `this.isim` ile nesneye özel olarak kendini tanıtacağı bir cümle bastırdık.

`main` fonksiyonu içerisinde de, `kisi1` adında bir insan nesnesi oluşturduk ve içerisine yapıcıya gidecek olan parametre değerlerini girdik. Hemen aşağısındaki koda dikkat edelim. `kendiniTanit` fonksiyonu `insan` sınıfına ait olduğu için ve `kisi1` nesnesi de `insan` sınıfından türetildiği için `kendiniTanit` fonksiyonunu `kisi1` nesnesine iliştirdik.

