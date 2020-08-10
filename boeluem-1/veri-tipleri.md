# Veri Tipleri

Dart programlama dilinden 5 ana veri tipi vardır.

1. Number
2. String
3. Boolean
4. List
5. Map

## 1. Number

**Number** ana tipi **numerik** değişkenleri hafızada tutmak içindir. İkiye ayrılır:

### 1.1 Integer

Tam sayılar için kullanılan tiptir. `int` terimi ile kullanılır.

```dart
int sayi = 10;
```

### 1.2 Double

Küsuratlı sayılar için kullanılan tiptir. `double` terimi ile kullanılır.

```dart
double sayi = 5.21;
```

## 2. String

String tipi metinsel ifadeleri hafızada tutmak için kullanılır. `String` terimi ile kullanılır.

```dart
String metin = "Merhaba";
```

## 3. Boolean

**Boolean** veri tipi mantıksal ifadeyi hafızada tutmak için kullanılır. `bool` terimi ile kullanılır.

```dart
bool online = true;
```

## 4. List

**List** veri tipi liste oluşturmamızı sağlar. `List` terimi ile kullanılır.

```dart
List isimler = ["kaan", "erkay", "altan"];
```

## 5. Map

**Map** veri tipi anahtarlı listeler oluşturmamızı sağlar. `Map` terimi ile kullanılır.

```dart
Map kisi = {"isim": "Kaan", "soyisim": "Kuşcu"};
```

## Dynamic ve Var ile Değişken Tanımlama

### 1. Var

**Var** ile atama yaparsak değişkenin tipini belirmemiz gerekmez. Yorumlayıcı yorumlama esnasında verilen değere göre değişkenin tipini belirler. `var` terimi ile kullanılır.

```dart
var degisken1 = "metin";
var degisken2 = 156;
var degisken3 = false;
```

### 2. Dynamic

**Dynamic** veri tipi değerin tipinin yorumlayıcı tarafından algılanmasını sağlar. Var'dan farkı içerisine başka türde değer atandığında değişken yeni atanan değerin tipine dönüşür. `dynamic` terimi ile kullanılır.

```dart
 dynamic degisken = "metin";
 dynamic degisken = 156;
 dynamic degisken = false;
```

