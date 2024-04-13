# Variables (Değişkenler)

**`let`**, **`var`** ve **`const`** JavaScript'te değişken tanımlamak için kullanılan üç farklı anahtar kelimedir. Bunlar, değişkenin nasıl davrandığı ve kapsamıyla ilgili farklılıklar gösterirler. İşte her birinin özellikleri:

 **var**:
- ES5 (ECMAScript 5) ile gelen bir değişken tanımlama anahtarıdır.
- Var ile tanımlanan değişkenler fonksiyon kapsamında ya da global kapsamda olabilir.
- Var, aynı isimde birden fazla değişken tanımlanmasına izin verir.
- Var ile tanımlanan değişkenler, deklarasyon öncesi kullanılabilir (hoisted).

**let**:
- ES6 (ECMAScript 2015) ile gelen bir değişken tanımlama anahtarıdır.
- Let ile tanımlanan değişkenler blok kapsamında olabilir (if, for, while gibi).
- Let, aynı isimdeki değişkenin tekrar tanımlanmasına izin vermez.
- Let ile tanımlanan değişkenler, deklarasyonlarına ulaşılana kadar "temporal dead zone" adı verilen bir süre boyunca erişilemezler.
- Eğer bir değişkene değer atanmazsa, varsayılan olarak undefined olur.

**const**:
- ES6 ile gelen bir değişken tanımlama anahtarıdır.
- Const ile tanımlanan değişkenler sabittir, yani bir kez atandıktan sonra değerleri değiştirilemez.
- Const ile tanımlanan değişkenler blok kapsamında olabilir.
- Const ile tanımlanan bir nesne veya dizi, referansı değiştirilemese de içeriği değiştirilebilir.













