# Get ve Set Fonksiyonları

`Get` ve `Set` değişkenler üzerinde işlem yapabilmemizi sağlayan basit fonksiyonlardır. **Get** fonksiyonumuz değer döndürür. **Set** fonksiyonumuz da değer atar.

```dart
class insan {
  String kisiIsim;

  String get isim {
    return kisiIsim;
  }

  void set isim(String i) {
    this.kisiIsim = i;
  }

  insan(this.kisiIsim);
}

main() {
  insan kisi1 = insan("Kaan");
  print(kisi1.isim); //get işlemi
  kisi1.isim = "Erkay"; //set işlemi
}
```

Yukarıdaki kodları incelediğimizde;

{% hint style="info" %}
Farkettiyseniz **kisi1** nesnesini oluşturuyorken **new** terimini kullanmadık. Bu terim **Dart 2.2** beri zorunlu değildir.
{% endhint %}

  
`insan` sınıfımızın içinde `String get isim` ile **String** tipinde değer döndüren bir fonksiyon oluşturduk. Bu fonksiyonumuz **get** fonksiyonu olduğu için parametreler için paranteze sahip olmayacaktır. **get** fonksiyonumuz `kisiIsim` değerini döndürüyor.

**set** fonksiyonumuz ise `void`'tir. Çünkü bir değer döndürmez. **get** ve **set** fonksiyonlarının isimleri aynı olmak zorundadır. **set** fonksiyonu atama işlemi yapacağı için parametre alır.

`main` fonksiyonuna baktığımızda, `kisi1` adında `insan` nesnesi örneği oluşturduk. `print` fonksiyonu içerisinde `kisi1.isim` yazarak **get** işlemi yaptık. Hemen aşağısında `kisi1.isim = "Erkay";` yazarak **set** işlemi yaptık.

{% hint style="warning" %}
Set işlemi yapılırken parametre parantezi açılmaz. Değer atama şeklinde yapılır.
{% endhint %}

{% hint style="danger" %}
**Yanlış:** `kisi1.isim("Erkay");`
{% endhint %}

{% hint style="success" %}
**Doğru:** `kisi1.isim = "Erkay";`
{% endhint %}

