# Fonksiyonlar

Fonksiyonlar, okunabilir, düzenlenebilir ve yeniden kullanılabilir kod blokları oluşturmamızı sağlar. Bu kod bloklarının içerisinde işlemler yapabiliriz.

Fonksiyonlar tanımlandıktan sonra başka bir yerden çağrılabilir. Bu özelliği kod bloğunu yeniden kullanılabilir yapar. Ayrıca kodun okunabilirliğini arttırır.

## Adımlar 

1. Fonksiyonun Tanımlanması
2. Fonksiyonun Çağrılması
3. Fonksiyonun Değer Döndürmesi
4. Fonksiyonun Parametresi

### 1. Fonksiyonun Tanımlanması

Fonksiyonun tanımlanması aşağıdaki gibi yapılır.

```dart
void merhaba() {
  print("merhaba");
}
```

Yukarıda ekrana `"merhaba"` yazan bir fonksiyon oluşturduk. Bu fonksiyonumuzu **merhaba** olarak adlandırdık.

### 2. Fonksiyonumuzun Çağrılması

Yukarıdaki merhaba fonksiyonunu kullanmak istersek aşağıdaki gibi yaparız.

```dart
void merhaba() {
  print("merhaba");
}

void main() {
  merhaba();
}
```

Yukarıda gördüğünüz gibi **main** fonksiyonu içerisinde **merhaba** fonksiyonunu kullandık.

### 3. Fonksiyonun Değer Döndürmesi

Fonksiyonlar bir eylem gerçekleştirmek yerine bize bir değer de döndürebilir. Bu işlemi `return` terimi ile yaparız.

```dart
int sayi() {
  return 10;
}

void main() {
  print(sayi());
}
```

Yukarıdaki kodları incelediğimizde, ilk gördüğümüz farklılık, bu sefer `void` terimi ile değil de `int` terimi ile fonksiyon oluşturduk. Bunun sebebi `sayi()` fonksiyonunda `return` ettiğimiz değer **integer** tipinde olmasıdır. Fonksiyon oluştururken, eğer bir değer döndürecekse fonksiyon isminden önce **return** tipini belirtmemiz gerekir.

#### Peki void nedir?

`void` terimini ise fonksiyonumuz bir değer döndürmüyorsa kullanırız. Dart'ta bir fonksiyonda `return` yoksa `return tipi` kullanmamızda zorunlu değildir.

```dart
merhaba() {
  print("merhaba");
}

main() {
  merhaba;
}
```

Yukarıda gördüğünüz gibi, aslında `void` yazmamıza gerek yok.

Özet olarak, eğer fonksiyon bir değer döndürüyorsa dönecek değerin tipi belirtiriz. Değer döndürmüyorsa `void` yazarız veya hiçbir şey yazmayız.

### 4. Fonksiyon Parametresi

Parametreler değerleri işlemlere iletmek için kullanılır. Yani bir fonksiyona işlemlerinde kullanması için parametreler yollayabiliriz.

```dart
int topla(int a, int b) {
  return a + b;
}

main() {
  print(topla(5, 10));
}
```

Kodlarımıza bakalım;

`topla` adında bir fonksiyon oluşturduk. bu fonksiyonun başta `int` tipinde bir değer döndüreceğini belirttik. Parantez içine baktığımızda `int a` ve `int b` terimlerini görüyoruz. Bunlar bizim parametrelerimiz. Bu parametreleri fonksiyonumuzun içerisinde topladık ve `return` ettik.

`main` fonksiyonu içerisinde de `topla` fonksiyonumuza iki değer girerek çağırıp ekrana bastırdık.

#### Fonksiyon Parametreleri Hakkında Tüyo

Parametreleri tanımlarken aşağıdaki gibi de tanımlayabiliriz.

```dart
int topla(int a, b) {
  return a + b;
}
```

`b`'nin tipini yazmadık, çünkü tipini bir önceki parametrenin tipi olarak belirlendi.

## Varsayılan Fonksiyon Parametreleri

Fonksiyondaki parametrelere girilmemesi dahilinde otomatik değer atanabilir. Örneğimiz;

```dart
int carp(int a, [int b = 2]) {
  return a * b;
}

main() {
  print(carp(5)); //10
  print(carp(5, 3)); //15
}
```

`carp` fonksiyonunu incelediğimizde, `a` adında `interger` tipinde bir parametre oluşturduk. Köşeli parantez içerisine `b` değişkeni tanımladık ve `2` değerini verdik. Yani `b` parametresinin girilmemesi durumunda `b` parametremizin değeri `2` olacaktır.

## Belirli Parametreyi Girme

```dart
int carp({int a, b}) {
  return a * b;
}

main() {
  print(carp(a: 5, b: 4));
}
```

`carp` fonksiyonunun parametrelerini tanımlıyorken, parantez içerisine ayrıca süslü parantez koyduğumuza dikkat çekmek isterim. Böyle fonksiyon başka bir yerden çağrılırken, tıpkı `map` kullanımındaki gibi değer yollayacağımız parametreyi de belirtiriz. 

