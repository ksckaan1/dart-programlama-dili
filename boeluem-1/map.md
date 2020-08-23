# Map

**Map**, birden fazla boyutu olan **List**'tir. Örnek:

```dart
Map isimler = {1: "Kaan", 2: "Erkay", 3: "Altan", 4: "Emir"};
```

Yukarıda 2 boyutlu `map` örneği verilmiştir. Çok boyutlu bir örnek verecek olursak:

```dart
Map isimler = {
 1: {"isim": "Kaan", "soyIsim": "Kuşcu", "yas": 23},
 2: {"isim": "Emir Alper", "soyIsim": "Babur", "yas": 27},
 3: {"isim": "Altan", "soyIsim": "Aydemir", "yas": 22}
};
```

`Map` üzerinde istenilen bölgeyi göstermek için:

```dart
print(isimler[1]); // {isim: Kaan, soyIsim: Kuşcu, yas: 23}
print(isimler[1]["isim"]); // Kaan
```

## Map Fonksiyonları

### isEmpty

Map boş ise **true** verir.

```dart
print(isimler.isEmpty); // false
```

### isNotEmpty

Map boş değilse **true** verir.

```dart
print(isimler.isNotEmpty); // true
```

### keys

Anahtarları listeler.

```dart
print(isimler.keys); // (1, 2, 3)
```

### lenght

Map'in uzunluğunu verir.

```dart
print(isimler.length); // 3
```

### values

keys'in tersi olarak değerleri listeler.

```dart
print(isimler.values); // ({isim: Kaan, soyIsim: Kuşcu, yas: 23}, {isim: Emir Alper, soyIsim: Babur, yas: 27}, {isim: Altan, soyIsim: Aydemir, yas: 22})
```

### addAll

Başka bir Map'i ekler. Aynı değerler var ise üzerine yazar.

```dart
main() {
  Map isimler = {
    1: {"isim": "Kaan", "soyIsim": "Kuşcu", "yas": 23},
    2: {"isim": "Emir Alper", "soyIsim": "Babur", "yas": 27},
    3: {"isim": "Altan", "soyIsim": "Aydemir", "yas": 22}
  };
  Map yeniIsimler = {
    4: {"isim": "Gökhan", "soyIsim": "Bingül", "yas": 26},
    5: {"isim": "İsmail", "soyIsim": "Tunç", "yas": 22},
    6: {"isim": "Emre", "soyIsim": "Gülşen", "yas": 23}
  };
  isimler.addAll(yeniIsimler);
  print(isimler);
}
```

> {1: {isim: Kaan, soyIsim: Kuşcu, yas: 23}, 2: {isim: Emir Alper, soyIsim: Babur, yas: 27}, 3: {isim: Altan, soyIsim: Aydemir, yas: 22}, 4: {isim: Gökhan, soyIsim: Bingül, yas: 26}, 5: {isim: İsmail, soyIsim: Tunç, yas: 22}, 6: {isim: Emre, soyIsim: Gülşen, yas: 23}}

### clear

Map'in içini boşaltır.

```dart
print(isimler); // {}
```

### containsKey

Anahtarı içerip içermediğini kontrol eder.

```dart
print(isimler[1].containsKey("isim")); // true
```

### containsValue

Değeri içerip içermediğini kontrol eder.

```dart
print(isimler[1].containsValue("Kaan")); // true
```

### forEach

Map'in eleman sayısına göre döndü işlemi yapar. forEach fonksiyonu 2 parametre alır. 1. anahtar parametresi, 2. değer parametresidir.

```dart
isimler.forEach((anahtar, deger) {
    print(anahtar.toString() + ". anahtarda : " + deger.toString());
});
```

> 1. anahtarda : {isim: Kaan, soyIsim: Kuşcu, yas: 23}
> 2. anahtarda : {isim: Emir Alper, soyIsim: Babur, yas: 27}
> 3. anahtarda : {isim: Altan, soyIsim: Aydemir, yas: 22}

### remove

Belirtilen anahtardaki değeri kaldırır.

```dart
isimler.remove(2);
print(isimler);
```

> {1: {isim: Kaan, soyIsim: Kuşcu, yas: 23}, 3: {isim: Altan, soyIsim: Aydemir, yas: 22}}

### update

Belirtilen anahtardaki değeri günceller.

```dart
isimler.update(
      2, (value) => {"isim": "Cüneyt", "soyIsim": "Ayder", "yas": 28});
print(isimler);
```

> {1: {isim: Kaan, soyIsim: Kuşcu, yas: 23}, 2: {isim: Cüneyt, soyIsim: Ayder, yas: 28}, 3: {isim: Altan, soyIsim: Aydemir, yas: 22}}

### Diğerleri

**updateAll** = Tüm değerleri günceller.

**runtimeType** = Çalışma zamanındaki veri tipini gösterir.

