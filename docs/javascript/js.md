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

## Loops (Döngüler)

### **for Loop - for Döngüsü**

- Belirli bir koşul sağlandığı sürece belirli bir kod bloğunu tekrarlamak için kullanılır.
- Genellikle bir başlangıç değeri, bir koşul ve bir artış/değişim adımı içerir.

```jsx
const countries = ['Finland', 'Sweden', 'Norway', 'Denmark', 'Iceland']
const newArr = []
for(let i = 0; i < countries.length; i++){
  newArr.push(countries[i].toUpperCase())
}

console.log(newArr)  // ["FINLAND", "SWEDEN", "NORWAY", "DENMARK", "ICELAND"]

```

### **while loop - while Döngüsü**

- while anahtar kelimesinin yanında belirtilen şarta doğru olduğu sürece çalışan bir döngü türüdür. Eğer koşul sürekli doğru çıkacak şekilde ayarlanırsa while döngüsü uygulama kasten kesilmediği sürece sonsuza kadar devam edebilir. Bu yüzden buraya dikkat etmek gerekebilir.

```jsx
let i = 0
while (i <= 5) {
  console.log(i)
  i++
}

// 0 1 2 3 4 5

```

### **do while loop do while döngüsü**

- do while döngüsü Koşul ile belirtilen alanın doğru olup olmadığına bakmadan kod bloğunu bir kez çalıştırır ve daha sonra Koşul ile belirtilen alan doğru (true) olduğu sürece kod bloğunun çalışması için kullanılır.

```jsx
let i = 0
do {
  console.log(i)
  i++
} while (i <= 5)

// 0 1 2 3 4 5

```

### **for of loop - for of döngüsü**

- ES6, geleneksel bir döngüden daha basit olan bir döngü olan yeni bir döngü yöntemi sunar ve her tür için ve giriş döngülerinin eksikliklerini telafi eder.
- `for..of` Deyimi, yinelenen nesneler üzerinde yinelemek için bir döngü oluşturur. ES6'da tanıtılan `for..of` döngü , yeni yinelemeli protokollerin yerini alır. `for..in` ve `forEach()` destekler. `for..of` Array (Diziler), String (Metinler), Map (Haritalar), Set (Kümeler), Array benzeri nesneler (örneğin arguments veya NodeList), ve diğer yinelenen veri yapıları arasında yineleme yapmanızı sağlar.

```jsx
let sum = 0
for (const num of numbers) {
  sum = sum + num  
  // daha pratik kullanım için, sum += num
  // bundan sonra pratik olan bu syntax türünün kullanacağız(+=, -=, *=, /= etc)
}

```

### *break ve continue*

- Break, bir döngüyü kesmek için kullanılır.
- Belirli bir döngü aşamasını atlamak için `continue` anahtar kelimesi kullanılır.

```jsx
for(let i = 0; i <= 5; i++){
  if(i == 3){
    break;
  }
  console.log(i)
}

// 0 1 2

i değeri 3 sayısına eşit olduğunda döngüyü durdurur


for(let i = 0; i <= 5; i++){
  if(i == 3){
    continue
  }
  console.log(i)
}

// 0 1 2 4 5

```

### **“switch” cümleleri**

Türkçe olarak buradaki anlamıyla “koşullu ifade” demektir.

Switch cümleleri if cümleleri haline de getirilebilirler.

Daha açıklayıcı ve değerleri birçok farklı şekilde karşılaştırabilir

```jsx
let a = 2 + 2;

switch (a) {
  case 3:
    alert( 'Çok kısa' );
    break;
  case 4:
    alert( 'Kesinlikle!' );
    break;
  case 5:
    alert( 'Çok büyük' );
    break;
  default:
    alert( "Böyle bir değeri bilmiyorum." );
}
```

Başlangıçta switch cümlesi a değişkenini ilk önce 3 case'i ile karşılaştırır. Bu karşılaştırma yanlış olduğundan ikinciye geçer.

4 ise eşitliği sağlar 4’ten itibaren en yakın break’e kadar olan bölüm çalışır.

**Eğer `break` konulmazsa sonraki `case` de hiçbir kontrol olmadan çalışır.**

## Functions
Bir fonksiyon, belirli bir görevi gerçekleştirmek üzere tasarlanmış ve yeniden kullanılabilir bir kod bloğu veya programlama tanımıdır.

Bir fonksiyon, ”function” anahtar kelimesi ardından gelen o fonksiyona ait fonksiyon ismi ve parantezler ile tanımlanır. Bu paranteler fonksiyona parametre atayabilmemizi sağlar. Şayet fonksiyon parametre alırsa bu parametre fonksiyon scope'u içerisinde geçerli olan bir değişkendir. Farklı bir kullanım olarak da bu parametreye default değerler atayabiliriz. Eğer bir fonksiyon yardımı ile veri taşımak istiyorsak söz konusu fonksiyonun belirli bir veri türünü geriye değişken olarak döndürmesi gerekir. Daha sonra dönen bu değişkeni bir başka değişkene atayarak kullanabilir.

Fonksiyon kullanmanın avantajları:

- temiz ve okunması kolay
- yeniden kullanılabilir
- kolay test edilir

Bir fonksiyon birkaç şekilde tanımlanabilir:

- *Klasik Declaration function*
- *Expression function*
- *Anonymous function*
- *Arrow function*

**Klasik Fonksiyon Tanımlama:**
```jsx
//parametresiz fonksiyon tanımıı
function functionName() {
  // istenilen kod parçası
}
functionName() // fonksiyon, fonksiyon adı ve parantezler ile çağırılır
```
**Anonymous Function:**
```jsx
const anonymousFun = function() {
  console.log(
    'İsimsiz bir fonksiyonum ve değerim anonim olarak saklanıyor'
  )
}
```
**Expression Function:**
Expression function, isimsiz fonksiyonlardır. İsimsiz bir fonksiyon oluşturduktan sonra bir değişkene atayarak kullanırız. Fonksiyondan bir değer geri döndürmek için değişkeni çağırmalıyız. Örnek vemrek gerekirse.
```jsx

// Function expression
const square = function() {
  console.log("Bu bir expression function türünde fonksiyondur")
}
```
**Parametresiz ve dönüş değeri olamayan fonksiyon:**
Fonksiyon, parametre olmadan tanımlanabilir. (Şu ana kadar tanımladıklarımız zaten parametresizdi)
```jsx
function square() {
  let num = 2
  let square = num * num
  console.log(square)
}

square() // 4

// parametresiz fonksiyon örnek 2:
function addTwoNumbers() {
  let numOne = 10
  let numTwo = 20
  let sum = numOne + numTwo

  console.log(sum)
}

addTwoNumbers() // fonksiyon, kendisine verilen isim ile çağırılmalı
```
**Bir değer döndüren fonksiyon:**
Fonksiyonlar geriye bir değer döndürebilir. bu işlemi `return` anahtar kelimesini kullanarak sağlarız. Normal fonksiyondan farklı olarak bir field'a atanabilir veya bir metot içerisinde parametre olarak kullanılabilir.

`return` fonksiyon içerisinde her yerde kullanılabilir. Kod `return` satırına eriştiğinde fonksiyon durur ve değer fonksiyonun çağırıldığı yere geri gönderilir.

Bir fonksiyon içerisinde birden fazla `return` fonksiyonu da olabilir.
```jsx
function printFullName (){
      let firstName = 'Asabeneh'
      let lastName = 'Yetayeh'
      let space = ' '
      let fullName = firstName + space + lastName
      return fullName
}
console.log(printFullName())
```
**Parametreli fonksiyon:**
Bir fonksiyonda farklı veri türlerini (number, string, boolean, object, function) parametre olarak geçebiliriz.

Parametrelere isteğe bağlı olarak veri paslanabilir. Bunlara *fonksiyon argümanları* da denir.
```jsx
// İki sayıyı toplayan bir fonksiyon
function toplama(sayi1, sayi2) {
    return sayi1 + sayi2;
}

// Fonksiyonu kullanarak toplama işlemi gerçekleştirme
var sonuc = toplama(5, 3);
console.log("Sonuç:", sonuc); // Çıktı: 8
```

**Kendi kendini çağıran fonksiyon**
Kendi kendini çağıran işlevlerin yararı, global ad alanını karıştırmadan (herhangi bir global bildirmeden) kodu bir kez yürütmemize olanak vermeleridir.

Kendi kendine çağrılan (recursive) fonksiyonlar, bir fonksiyonun kendini çağırmasıyla gerçekleşen bir programlama tekniğidir. Bu tekniği kullanarak genellikle belirli bir problemi daha küçük alt problemlere bölerek çözebiliriz.

Örneğin, faktöriyel hesaplama işlemi için bir kendi kendine çağrılan fonksiyon örneği verelim:

```jsx
function faktoriyel(n) {
    if (n === 0) {
        return 1; // 0! = 1
    } else {
        return n * faktoriyel(n - 1); // n! = n * (n-1)!
    }
}

// Faktöriyel hesaplama işlemi
var sonuc = faktoriyel(5); // 5! = 5 * 4 * 3 * 2 * 1 = 120
console.log("5 faktöriyel:", sonuc); // Çıktı: 120
```

**Arrow Function**
Klasik fonksiyona alternatif olarak kullanılan arrow function sözdiziminde ufak bir farklılık vardır. `function` anahtar kelimesi yerine `=>` işareti kullanılır.

Sırasıyla aynı fonksiyonun klasik ve arrow function halini yazalım.

```jsx
function square(n) {
  return n * n
}

console.log(square(2)) // 4

const square = n => {
  return n * n
}

console.log(square(2))  // -> 4

// kod bloğumuzda sadece bir satır kod varsa bu fonksiyon şu şekilde yazılabilir.
const square = n => n * n  // -> 4
```



