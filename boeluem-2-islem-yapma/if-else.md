# If - Else

If ve Else kelimelerinin Türkçe karşılığına bakacak olursak;

**If :** Eğer, **Else :** Yoksa anlamına gelir. **If-Else** akışı koşullandırmalar için kullanılır. Diğer dillerin aksine koşul parametresi parantezler içine yazılmaz. Teorik kısmı bırakıp uygulama kısmına geçelim ki daha anlaşılır olsun.

```dart
if (koşul){
  //koşul sağlandığında yapılacak işlemler
}else{
  //koşul sağlanmadığında yapılacak işlemler
}
```

Yukarıdaki kod tanımına göre örnek bir program yazalım;

```dart
main() {
  int i = 5;
  if (i == 5) {
    print("i'nin değeri 5'tir.");
  } else {
    print("i'nin değeri 5 değildir.");
  }
}
```

Yukarıdaki kodları inceleyelim. `i`’nin değerini `5` verdik. `if` teriminin sağında `i`’nin `5` 'e eşitliği koşulunu sorguladık. Eşitse ekrana `i’nin değeri 5’tir.` yazısını bastıracak. Değilse `i’nin değeri 5 değildir.` yazısı bastıracak. `i`’nin değeri `5` olduğu için ekrana `i’nin değeri 5’tir.` yazısını bastırdı. If-Else akışında else kullanmamamız else’nin kod bloğunu boş bırakmamız ile aynı anlama gelir.

```dart
main() {
  int i = 5;
  if (i == 5) {
    print("i'nin değeri 5'tir.");
  }
}
```

Yukarıda sadece **if** deyimini girdik. **Else**’yi girmedik. Burada sonuçlanan olay, **i**’nin değeri **5**'e eşitse `i'nin değeri 5'tir.` yazısını ekrana bastırır. **Else** deyimini girmediğimiz için şartın sağlanmaması durumunda hiçbir işlem gerçekleşmez. Çıktımız **i**’nin değeri **5**'e eşit olduğu için `i’nin değeri 5'tir.` çıkar.

**ELSE-IF KULLANIMI**

**If-Else** akışında birden fazla koşul kontrolü ekleyebiliriz. Bunu **else if** deyimi ile yapabiliriz. Kısaca bakacak olursak;

```dart
main() {
  int i = 3;
  if (i == 5) {
    print("i'nin değeri 5'tir.");
  } else if (i == 3) {
    print("i'nin değeri 3'tür.");
  } else {
    print("i'nin değeri bilinmiyor");
  }
}
```

`else if` deyiminin yazılışını da gördük. Açıklamaya gelirsek, `else if` deyimi kendinden önceki deyimin koşulunun sağlanmaması halinde bir sonraki koşulu kontrol ettirir. **If-Else** akışında istenildiği kadar `else if` deyimi eklenebilir.

  
**Koşullar İçerisinde Operatör Kullanımı**  
Koşullar içerisinden mantıksal ve ilişkisel operatörler kullanılabilir. Operatörleri görmüştük. Operatör kullanarak örnekler yapalım.

```dart
main() {
  int a = 1, b = 3, c = 5;

  if (a != b) {
    print("a eşit değildir b");
  }
  if (a < c) {
    print("a küçüktür c");
  }
  if (a < b && b < c) {
    print("a küçüktür b ve b küçüktür c");
  }
}
```

Çıktımız aşağıdaki gibi olacaktır:

> a eşit değildir b  
> a küçüktür c  
> a küçüktür b ve b küçüktür c

