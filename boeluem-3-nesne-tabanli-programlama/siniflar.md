# Sınıflar

## Sınıf Oluşturma

Sınıflar diğer birçok dildeki gibi `class` terimi ile oluşturulur.

```dart
class insan {
  String isim;
  int yas;
  double kilo;
}

main() {
  insan kisi1 = new insan();
}
```

Yukarıda bir `insan` sınıfı oluşturduk. Bu sınıf **isim**, **yas** ve **kilo** gibi özellikleri vardır. Tıpkı bir insanda bulunan özellikler gibi.

Hemen aşağısında, **kisi1** adından **insan** sınıfında bir nesne ürettik. Artık **kisi1** nesnesi bir insan oldu 😉

Peki `kisi1`'in böyle özellikleri var ama bu özelliklerin değerleri yok mu? Tabi ki olacak.

```dart
class insan {
  String isim = "Kaan";
  int yas = 23;
  double kilo = 78.2;
}

main() {
  insan kisi1 = new insan();
}
```

Artık `kisi1` tamamen insan oldu diyebiliriz. `print(kisi1.isim);` yazarak `kisi1`'in isim değişkenini yazdırabiliriz. Ama olaya biraz dikkat ettiğimizde değerlerin `kisi1`'e ait değil de insan sınıfında ait olduğunu görebiliriz. Yani `insan` sınıfı için oluşturulmuş nesnelerin varsayılan değerini girmiş olduk. Çözümümüz Constructors \(Yapıcılar\);

## Constructors \(Yapıcılar\)

Yapıcılar bir sınıf nesnesi üretirken değerlerin tanımlanmasında kullanılır. Örneğimiz:

```dart
class insan {
  String isim;
  int yas;
  double kilo;

  insan(String isimGiris, int yasGiris, double kiloGiris) {
    isim = isimGiris;
    yas = yasGiris;
    kilo = kiloGiris;
  }
}

main() {
  insan kisi1 = new insan("Kaan", 23, 78.2);
  print(kisi1.isim);
}
```

Yapıcılar sınıfların içerisine fonksiyon olarak tanımlanır. Bir fonksiyonun yapıcı fonksiyon olması için sınıf ile aynı isme sahip olması gerekir. Yani `insan` sınıfının yapıcısı `insan()` fonksiyonu olmalıdır. Yapıcı fonksiyonlardaki mantık, dışarıdan alınan değerleri sınıf içerisindeki değişkenlere yerleştirmektir. Yapıcı fonksiyondaki parametrelerin isimleri ile sınıf değişkenlerinin isimlerinin aynı olmadığına dikkat çekmek isterim. Bu işlemi `this` işaretçisi ile de yapabiliriz. 

## This işaretçisi nedir?

**This** işaretçisi, sınıfa özel tanımlı değişkenleri kullanabilmeyi sağlayan işaretçidir. Yapıcımızı bir de `this` ile oluşturalım.

```dart
insan(String isim, int yas, double kilo) {
  this.isim = isim;
  this.yas = yas;
  this.kilo = kilo;
}
```

Yukarıdaki `this` şu işlemi yapıyor. **this = bu**. `isim` parametresinden gelen değer, `this.isim` ile bu sınıfın `isim` değişkenine atansın.

## This ile Yapıcı oluştururken Kolay Yöntem

```dart
insan(this.isim, this.yas, this.kilo) {}
```

Yukarıdaki yapıcıyı oluştururken parametreleri `this` işaretçisi ile yazdık. Böylece atama işlemine gerek kalmadan parametreler üzerinden atanmasını sağladık.

## Sınıf Nesnesi Oluştururken Belirli ve Varsayılan Yapıcı Parametresi Girme

{% page-ref page="../boeluem-2-islem-yapma/fonksiyonlar.md" %}

Fonksiyonlar konusunda gördüğümüz gibi parametrelere değer yollarken hangi değişkene yollayacağımızı seçebiliriz.

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
}

main() {
  insan kisi1 = new insan(isim: "Erkay", kilo:78.2);
}
```

`main` fonksiyonuna baktığımızda,

`kisi1` adında insan nesnesi oluştururken yapıcı fonksiyona sadece `isim` ve `kilo` değerlerini yolladık. `yas` değişkeninin değeri yapıcı fonksiyonda varsayılan değer aldı.

## İsimlendirilmiş Yapıcılar

Eğer sınıfımıza birden fazla yapıcı eklemek istiyorsak isimlendirilmiş yapıcıları kullanırız. Örnek:

```dart
class insan {
  String isim;
  int yas;
  double kilo;
  insan(this.isim, this.yas, this.kilo);

  insan.bos() {
    this.isim = "Boş";
    this.yas = 0;
    this.kilo = 0;
  }
}

main() {
  insan kisi1 = new insan.bos();
}
```

`insan` sınıfımız hem `insan` adlı yapıcı fonksiyona sahip, hem de `insan.bos` adında isimlendirilmiş yapıcı fonksiyona sahip. `insan.bos` yapıcı fonksiyonumuz `insan` sınıfından üretilen nesnede kullanıldığında değişkenlere boş bilgiler giriyor.

`main` fonksiyonumuzda nesne üretimini gözlemlediğimizde, nesnenin `insan.bos()` yapıcı fonksiyonu ile üretildiğini görüyoruz.

