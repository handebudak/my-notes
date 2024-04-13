# Conditionals (Koşullar)

### if

if bloğu ile tanımladığımız koşul eğer doğru yani true bilgi üretiyorsa if bloğu kapsamındaki kodlar işletilir eğer false üretirse işletilmez.

### else

if bloğunun true değer üretmediği durumda da bazı kodları çalıştırmak isteyebiliriz bu durumda else bloğunu kullanmalıyız.

### else if

Bazen de bir koşula bağlı olarak farklı farklı koşullar üretmek isteyebiliriz. Bu durumda else-if bloğunu kullanarak ekstra sorular sorma imkanına sahip oluruz.

```jsx
if (kosul1) {
  //  koşul 1 true ürettiğinde çalışır.
} else if (kosul2) {
  // kosul1 false olduğunda koşul2 ' e bakılır. koşul2 true ise çalışır.
} else {
  //  koşul1 ve koşul2 false ürettiğinde çalışır.
}
```

### Üçlü operatör (’?’)

`koşul` değerlendirildikten sonra eğer doğru döner ise `deger1` yanlış döner ise `deger2` sonuç değişkenine atanır.

```jsx
let sonuc = koşul ? deger1 : deger2

```