# Static

Sınıf yapısını oluşturuyorken, bazı nesnelerin dışarıyla olan etkileşimini ayarlamak gerekebilir.

`Static` ile oluşturulan değişken ve fonksiyonlara sınıf dışından erişilemezler. Örnek;

```dart
class insan {
  static String isim;
  
  static fonksiyonum() {
    print(isim);
  }
}
```

Yukarıdaki **insan** sınıfında **static insan** değişkeni oluşturduk. Bu değişken sadece sınıf içerisindeki işlemlerde kullanılabilecek. Aynı şekilde `fonksiyonum` 'da.



