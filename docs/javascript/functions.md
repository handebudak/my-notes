# Functions
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