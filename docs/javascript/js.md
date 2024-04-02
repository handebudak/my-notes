# JavaScript 

## Variables (Değişkenler)

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

## Data Types (Veri Tipleri)

***Primitif Veri Tipleri:***

 1. **String (Metin)**
- Metin değerlerini temsil eder.
- Örneğin: **`"Merhaba"`**, **`"Dünya"`**, **`"123"`** gibi.

2. **Number (Sayı)**
- Sayısal değerlerin temsil edilmesi için kullanılır.
- Örneğin: **`42`**, **`3.14`**, **`10`** gibi.

3. **Boolean (Mantıksal)**
- Sadece iki değer alabilir: **`true`** (doğru) ve **`false`** (yanlış).
- Genellikle karar verme süreçlerinde ve koşullu ifadelerde kullanılır.

4. **Undefined (Tanımsız)**
- Değer atanmamış bir değişkeni veya fonksiyon sonucu olmayan bir değişkeni temsil eder.
- Genellikle bir değişkenin tanımının yapılmadığı veya bir fonksiyonun geri dönüş değerinin belirtilmediği durumlarda ortaya çıkar.

5. **Null (Boş)**
- Bilerek atanmış boş bir değeri temsil eder.
- Örneğin, bir değişkenin hiçbir şeye işaret etmediği durumlarda null kullanılabilir.
    

 ***Non-Primitif Veri Tipleri:***

1. **Array (Dizi)**
- Bir dizi, sıralı bir koleksiyonu temsil eder.
- Öğeler, sıfırdan başlayarak indekslenir.
- Örneğin: **`[1, 2, 3, 4]`**, **`["elma", "armut", "portakal"]`** gibi.
2. **Object (Nesne)**
- Anahtar-değer çiftlerini içeren karmaşık bir veri yapısıdır.
- Anahtarlar bir dize (string) olmalıdır ve değerler herhangi bir JavaScript veri türü olabilir.
- Örneğin: **`{name: "Ahmet", age: 30, city: "İstanbul"}`** gibi.
3. **Symbol (Sembol)**
- ECMAScript 6 ile tanıtılan, benzersiz ve değiştirilemez bir veri türüdür.
- Genellikle nesne özelliklerini tanımlamak için kullanılır.
- **`Symbol()`** fonksiyonu ile oluşturulabilir: **`const mySymbol = Symbol();`**

Primitif veri tipleri, değerleri doğrudan saklar ve bellekte sabit boyutlarda depolanır. Non-primitif veri tipleri ise referansları saklar ve bellekte değişen boyutlarda depolanır. Bu fark, primitif ve non-primitif veri tiplerinin davranışlarını ve işlemlerini etkiler.

## Type Conversions (Tip Dönüşümleri)

**Implicit Conversion (Kapsayıcı Dönüşüm)**:

- JavaScript, bazı durumlarda veri tiplerini otomatik olarak dönüştürebilir.
- Örneğin, sayısal bir ifade ve metin birleştirildiğinde otomatik olarak sayısal ifade metine dönüştürülür.

```jsx
var sayi = 10;
var metin = "Sayı: " + sayi; // 10'u "10" şekline dönüştürür
```

**Explicit Conversion (Açık Dönüşüm)**:

- Bazı durumlarda, veri tiplerini belirli bir şekilde dönüştürmek isteyebiliriz.
- **`parseInt()`**, **`parseFloat()`**, **`String()`**, **`Number()`**, **`Boolean()`** gibi fonksiyonlarla bu dönüşümleri gerçekleştirebiliriz.

**ToString() Method**:

- Bir nesne veya değeri metin olarak dönüştürmek için kullanılır.

**ToNumber() Method**:

- Bir metni veya başka bir veri tipini sayıya dönüştürmek için kullanılır.

**ToBoolean() Method**:

- Bir nesneyi veya değeri boolean (mantıksal) bir değere dönüştürmek için kullanılır.
- Boş bir dize, sıfır, **`null`**, **`undefined`**, **`NaN`** gibi değerler false olarak kabul edilir; diğer durumlarda true olarak kabul edilir.

## Operators (Operatörler)

**Aritmetik Operatörler**:

- **`;`**   :Toplama operatörü
- **`-`**   : Çıkarma operatörü
- **`x`**   : Çarpma operatörü
- **`/`**   : Bölme operatörü
- **`%`**   : Mod (kalan) operatörü

**Atama Operatörleri**:

- **`=`** : Değer atama operatörü
- **`+=`** : Toplama atama operatörü
- **`=`** : Çıkarma atama operatörü
- **`=`** : Çarpma atama operatörü
- **`/=`** : Bölme atama operatörü
- **`%=`** : Mod atama operatörü

**Karşılaştırma Operatörleri**:

- **`==`** : Eşit mi?
- **`===`** : Kesinlikle eşit mi?
- **`!=`** : Eşit değil mi?
- **`!==`** : Kesinlikle eşit değil mi?
- **`>`** : Büyük mü?
- **`<`** : Küçük mü?
- **`>=`** : Büyük veya eşit mi?
- **`<=`** : Küçük veya eşit mi?

**Mantıksal Operatörler**:

- **`&&`** : Ve (and) operatörü
- **`||`** : Veya (or) operatörü
- **`!`** : Değil (not) operatörü

## Conditionals (Koşullar)

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

## Logical Operators (Mantıksal Operatörler)

1. **Ve Operatörü (&&)**:
- **`&&`** operatörü, iki koşulun da doğru olması durumunda ifadeyi doğru olarak değerlendirir.
- Her iki koşul da doğruysa, ifade doğru olur.
- Eğer en az bir koşul yanlışsa, ifade yanlış olur.
- Örneğin: **`if (x > 5 && y < 10) { ... }`**
2. **Veya Operatörü (||)**:
- **`||`** operatörü, iki koşuldan en az birinin doğru olması durumunda ifadeyi doğru olarak değerlendirir.
- Her iki koşul yanlışsa, ifade yanlış olur.
- Eğer en az bir koşul doğruysa, ifade doğru olur.
- Örneğin: **`if (x === 0 || y === 0) { ... }`**
3. **Değil Operatörü (!)**:
- **`!`** operatörü, bir koşulun tersini alır.
- Eğer koşul doğruysa, **`!`** operatörü onu yanlış olarak değerlendirir.
- Eğer koşul yanlışsa, **`!`** operatörü onu doğru olarak değerlendirir.
- Örneğin: **`if (!isLoggedin) { ... }`**