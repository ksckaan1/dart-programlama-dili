# Tür Dönüşümü

Dart üzerinde veri tiplerini birbirine dönüştürebiliriz.

### Örnek:

```dart
int sayi = 15;
String yazi = sayi.toString();
double sayi1 = 15.23;
int sayi2 = sayi1.toInt();
```

{% hint style="info" %}
`toString()` : String'e dönüştürme  
`toInt()` : Integer'a dönüştürme  
`toDouble()` : Double'a dönüştürme
{% endhint %}

Bir değişkenin veya sabitin veri tipini öğrenmek için `runtimeType` fonksiyonunu kullanabiliriz.

```dart
main() {
  int i = 5;

  print(i.runtimeType); //int
}
```

