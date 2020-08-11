# Arrow Fonksiyonlar

**Arrow** \(ok\) fonksiyonlar ile tek satırlık fonksiyonlar oluşturabiliriz. Bu şekilde daha kısa fonksiyonlar yazabiliriz.

```dart
int topla(int a, b) => a + b;

main() {
  print(topla(5, 10));
}
```

`topla` fonksiyonunun parametrelerine kadar normal fonksiyonlarla aynıdır. Daha sonrasında `=>` kullanarak tek satırlık işlem yapabiliriz. Dikkat ettiyseniz `topla` fonksiyonu `int` tipinde `return` ediyor. Fakat fonksiyonun hiçbir yerinde `return` terimi bulunmuyor. Çünkü gerek yok

