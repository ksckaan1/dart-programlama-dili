# List

Bu bölümde **List** veri tipini detaylıca inceleyeceğiz.

**List**, liste oluşturmamızı sağlayan bir veri tipidir. `List` terimi ile kullanılır.

```dart
List isimler = ["Kaan", "Erkay", "Altan", "Emir"];
```

## Index Nedir?

`Index`, **List** içindeki elemanların sıra numarasıdır. **Index** sırası 0'dan başlar. Yukarıdaki örneğe göre:

```dart
print(isimler[1]); //Erkay
```

## List Uzunluğu

`List` uzunluğunu `length` fonksiyonu \(getter\) iliştirilerek öğrenilebilir.

```dart
print(isimler.lenght); //4
```

## List Ters Çevirme

```dart
print(isimler.reversed); //(Emir, Altan, Erkay, Kaan)
```

## First ve Last

```dart
print(isimler.firt); //ilk indexi verir.
print(isimler.last); //son indexi verir.
```

## isEmpty ve isNotEmpty

`isEmpty` boşsa `true`, `isNotEmpty` boş değilse `true` döndürür.

```dart
print(isimler.isEmpty); //false
print(isimler.isNotEmpty); //true
```

## runtimeType

`List`'in veri tipini verir. Veri tipi belirlenmemişse `dynamic`'tir.

```dart
print(isimler.runtimeType); //List<dynamic>
```

## add

`List`'e eleman ekler.

```dart
List isimler = ["Kaan", "Erkay", "Altan", "Emir"];
isimler.add("Ahmet");
print(isimler); //[Kaan, Erkay, Altan, Emir, Ahmet]
```

## addAll

Başka bir `List`'teki elemanları ekler.

```dart
List isimler = ["Kaan", "Erkay", "Altan", "Emir"];
List yeniIsimler = ["Ahmet", "Mehmet", "Ali"];
isimler.addAll(yeniIsimler);
print(isimler);
//[Kaan, Erkay, Altan, Emir, Ahmet, Mehmet, Ali]
```

## asMap

`Map`'e dönüştürür.

```dart
List isimler = ["Kaan", "Erkay", "Altan", "Emir"];
print(isimler.asMap());
//{0: Kaan, 1: Erkay, 2: Altan, 3: Emir}
```

## clear

`List` içeriğini temizler.

```dart
List isimler = ["Kaan", "Erkay", "Altan", "Emir"];
isimler.clear();
print(isimler); // []
```

## fillRange

Belirlediğimiz index aralığını `null` ile doldurur. **Null** belirlenmemiş veri tipidir. Yani boştur.

```dart
 List isimler = ["Kaan", "Erkay", "Altan", "Emir"];
 isimler.fillRange(1, 3);
 print(isimler); //[Kaan, null, null, Emir]
```

## getRange

Belirlediğimiz aralığı verir.

```dart
List isimler = ["Kaan", "Erkay", "Altan", "Emir"];
print(isimler.getRange(1, 3)); // (Erkay, Altan)
```

## indexOf

Yazılan nesnenin indexini verir.

```dart
List isimler = ["Kaan", "Erkay", "Altan", "Emir"];
print(isimler.indexOf("Altan")); // 2
```

## insert

Belirlenen indexe eleman ekleme.

```dart
List isimler = ["Kaan", "Erkay", "Altan", "Emir"];
print(isimler); // [Kaan, Erkay, Altan, Emir]
isimler.insert(2, "Ali");
print(isimler); // [Kaan, Erkay, Ali, Altan, Emir]
```

## insertAll

Belirlenen indexe `List` ekleme.

```dart
List isimler = ["Kaan", "Erkay", "Altan", "Emir"];
List isimlerYeni = ["Ali", "Mehmet", "Ahmet"];
print(isimler); // [Kaan, Erkay, Altan, Emir]
isimler.insertAll(2, isimlerYeni);
print(isimler);
// [Kaan, Erkay, Ali, Mehmet, Ahmet, Altan, Emir]
```

## lastIndexOf

Aramaya sondan başlayarak yazılan elemanın indexini verir.

```dart
List isimler = ["Kaan", "Erkay", "Kaan", "Emir"];
print(isimler.lastIndexOf("Kaan")); // 2
```

## remove

Yazılan elemanı kaldırır.

```dart
List isimler = ["Kaan", "Erkay", "Altan", "Emir"];
  isimler.remove("Altan");
  print(isimler); // [Kaan, Erkay, Emir]
```

## removeAt

Belirtilen indexteki elemanı kaldırır.

```dart
List isimler = ["Kaan", "Erkay", "Altan", "Emir"];
isimler.removeAt(1);
print(isimler); // [Kaan, Altan, Emir]
```

## removeLast

`List`'in son elemanını kaldırır.

```dart
List isimler = ["Kaan", "Erkay", "Altan", "Emir"];
isimler.removeLast();
print(isimler); // [Kaan, Erkay, Altan]
```

## removeRange

Belirlenen aralığı kaldırır.

```dart
List isimler = ["Kaan", "Erkay", "Altan", "Emir"];
isimler.removeRange(1, 3);
print(isimler); // [Kaan, Emir]
```

## replaceRange

Belirtilen aralığı değiştirir.

```dart
List isimler = ["Kaan", "Erkay", "Altan", "Emir"];
isimler.replaceRange(1, 3, ["Ahmet", "Merhmet"]);
print(isimler); // [Kaan, Ahmet, Merhmet, Emir]
```

## setAll

Belirtilen indexten itibaren belirtilen `List` elemanlarının atanması.

```dart
List isimler = ["Kaan", "Erkay", "Altan", "Emir"];
List isimlerYeni = ["İsmail", "Ahmet", "Ali", "Gökhan"];
isimler.setAll(0, isimlerYeni);
print(isimler); // [İsmail, Ahmet, Ali, Gökhan]
```

## setRange

Belirtilen aralığa atama.

```dart
List isimler = ["Kaan", "Erkay", "Altan", "Emir"];
isimler.setRange(1, 3, ["İsmail", "Ali"]);
print(isimler); // [Kaan, İsmail, Ali, Emir]
```

## shuffle

`List`'i rastgele olarak karıştırır.

```dart
List isimler = ["Kaan", "Erkay", "Altan", "Emir"];
isimler.shuffle();
print(isimler); // [Emir, Erkay, Altan, Kaan]
```

## sort

List'i veri tipine göre sıralar.

```dart
List isimler = ["Kaan", "Erkay", "Altan", "Emir"];
isimler.sort();
print(isimler); // [Altan, Emir, Erkay, Kaan]
```

## sublist

`List`'i verilen indexten başlatır.

```dart
List isimler = ["Kaan", "Erkay", "Altan", "Emir"];
print(isimler.sublist(2)); // [Altan, Emir]
```

