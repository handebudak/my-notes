# Loops (Döngüler)

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