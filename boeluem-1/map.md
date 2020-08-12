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



