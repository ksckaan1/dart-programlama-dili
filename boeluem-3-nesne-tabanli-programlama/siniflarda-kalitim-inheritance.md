# Sınıflarda Kalıtım \(Inheritance\)

Bir sınıfa ait özellikleri başka bir sınıfta da kullanmak istiyorsak kalıtım özelliğinden faydalanabiliriz. Örnek:

```dart
class insan {
  String isim;
  int yas;
  double kilo;
}

class calisan extends insan {
  double maas;
}
```

`insan` adında bir sınıf oluşturduk ve bir insanda olacak özelliklerden referans alarak değişkenler oluşturduk.

`calisan` adında bir sınıf oluşturduk ve `extends insan` yazarak `insan` sınıfının özelliklerinden faydalanmasını sağladık. Sonuçta çalışanlar da bir insan 😉

Bir çalışanın özelliği olan maaş \(`maas`\) özelliğini ekledik. Yukarıdaki örneğimizde `calisan` sınıfı `insan` sınıfının özelliklerine de sahip olacaktır.

## Kalıtım İşleminde Yapıcı Fonksiyon Nasıl Kullanılır?

Şöyle uzun bir kod örneği görelim:

```dart
class insan {
  String isim;
  int yas;
  double kilo;
  insan(String isim, int yas, double kilo) {
    this.isim = isim;
    this.yas = yas;
    this.kilo = kilo;
  }
}

class calisan extends insan {
  double maas;

  //Yapıcı Fonksiyonumuza dikkat edin
  calisan(isim, yas, kilo, this.maas) : super(isim, yas, kilo);
  kendiniTanit() {
    print("Ad: " + this.isim);
    print("Yaş: " + (this.yas).toString());
    print("Kilo: " + (this.kilo).toString());
    print("Maaş: " + (this.maas).toString());
  }
}

main() {
  calisan kisi1 = new calisan("Kaan", 23, 78.2, 3400.25);
  kisi1.kendiniTanit();
}
```

Yine bir `insan` sınıfı oluşturduk. Bu sınıf her zaman ki gibi bir yapıcı fonksiyona sahip.

`calisan` sınıfı oluşturduk ve bu sınıfı `insan` sınıfından miras aldık.  `calisan` adlı yapıcı fonksiyonumuza dikkat ettiğimizde,

Parametreler içerisine `isim`, `yas` ve `kilo` isminde parametreler aldık. Bu parametreler miras aldığımız sınıftan geldiği için türlerini belirtmedik. Son parametremiz ise `this.maas`. `maas` değişkenini **this** ile kolayca atadık. Parametrelerin yanındaki `super` fonksiyonu ise miras aldığımız sınıftan gelen parametrelerdir.

Daha sonra `kendiniTanit` fonksiyonu oluşturarak `calisan` sınıfına ait bilgileri ekrana yazdırmasını sağlayan bir fonksiyon oluşturduk.

### Kalıtım İşleminde İsimli Yapıcı Fonksiyon Kullanma

Nasıl yazacağımızı görelim:

```dart
class calisan extends insan {
  calisan() : super.bos();
  // ···
}
```

