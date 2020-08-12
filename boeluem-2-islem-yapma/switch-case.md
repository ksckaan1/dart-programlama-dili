# Switch - Case

**Switch**, bir değişkeni anahtar olarak belirler. **Case** ise bu değişkenin durumunu kontrol eder. Mantık olarak **if-else**'e benzer. Farkı ise bunu sadece bir değişken üzerinde uygulamasıdır. Örneğimiz:

```dart
main() {
  int i = 5;
  switch (i) {
    case 0:
      print("i'nin değeri 0'dır.");
      break;
    case 5:
      print("i'nin değeri 5'tir.");
      break;
    case 10:
      print("i'nin değeri 10'dur.");
      break;
    default:
      print("i'nin değeri bilinmiyor.");
  }
}
```

`switch(i)` yazarak i değişkenini anahtar olarak belirledik. Aşağısındaki `case 0` ile **i**'nin değerinin **0** olup olmadığını sorguluyoruz. **0** ise **print** ile `"i'nin değeri 0'dır."` yazdırdık. **break**'in anlamı ise **case** doğru olduğunda diğer **case**'leri kontol etmemesi içindir. **default** ise **else** ile aynı mantıktadır.

```dart
main() {
  int i = 0;
  switch (i) {
    case 0:
      print("mesajım 1");
      continue durumum;
    case 5:
      print("mesajım 2");
      break;
    durumum:
    case 0:
      print("mesajım 3");
      break;

    default:
      print("mesajım 4");
  }
}
```

Yukarıda `continue`'nun kullanımına bir örnek vardık. İnceleyecek olursak;

`i` adlı integer tipinde `0` değeri olan bir değişken tanımladık. Bu değişkeni `switch`'e anahtar değişken olarak yazdık. Değişkenin değerinin `0` olması durumunda ekrana `"mesajım 1"` yazdırmasını istedik ve `continue durumum` yazarak durumum etiketinden devam etmesini istedik. Böylede `case 5`'i atlayarak `durumum:` etiketinden devam etti.

