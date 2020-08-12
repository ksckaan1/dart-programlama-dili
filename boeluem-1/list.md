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

