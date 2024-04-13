# Arrays (Diziler)
Değişkenlerin aksine, diziler *Çoklu değerleri* depolayabilirler. Dizi'deki her bir değer *index*'e sahiptir, ve her index *bellek adresindeki bir referans*'ı işaret eder. Bu *index'ler* kullanılarak her bir değere ulaşım sağlanabilir. Bir dizinin index'i *sıfır*'dan başlar ve dizinin son elemanının index'i, dizinin uzunluğundan bir eksiktir.

Bir dizi, sıralı ve değiştirilebilirdir. Farklı veri türlerinin bir koleksiyonudur. Bir dizi, tekrar edilen elemanların ve farklı veri türlerinin depolanmasına izin verir. Bir dizi boş olabilir veya farklı veri türü değerlerine sahip olabilir.

Objeler değerlerin anahtarlı bir şekilde koleksiyon halinde tutulmasını sağlar.

Fakat bazı durumlarda *sıralı koleksiyon* tutmak gerekebilir, 1., 2. ve 3. elemente ihtiyaç olabilir. Örneğin kullanıcıların, ürünlerin, HTML elementlerinin liste halinde tutulmasını istediğinizde;

Obje kullanmak mantıklı değildir, çünkü elemanların sırasını tutmaz bu objeler. Var olanların “arasına” yeni bir özellik girilemez. Objeler böyle kullanımlara uygun değildir.

**Boş bir dizi nasıl oluşturulur**
```jsx
let arr = new Array();
let arr = [];
```

**Diziler sıfır ile başlarlar**
```jsx
let meyveler = ["Elma", "Portakal", "Erik"];

alert( meyveler[0] ); // Elma
alert( meyveler[1] ); // Portakal
alert( meyveler[2] ); // Erik
```
**Elemanı değiştirmek mümkündür, Veya diziye yeni bir eleman eklemek mümkündür**
```jsx
meyveler[2] = 'Armut'; // Şimdi ["Elma", "Portakal", "Armut"]
meyveler[3] = 'Limon'; // Şimdi ["Elma", "Portakal", "Armut", "Limon"]
```
**Dizide bulunan elemanların boyutu length metodu ile öğrenilebilir:**
```jsx
let meyveler = ["Elma", "Portakal", "Erik"];

alert( meyveler.length ); // 3
```
**Dizi her türlü elemanı tutabilir.**
```jsx
// Karmaşık tipler
let arr = [ 'Elma', { isim: 'Ahmet' }, true, function() { alert('merhaba'); } ];

// Birinci indeksteki değeri al ve "isim" özelliğini görüntüle
alert( arr[1].isim ); // John

// 3. indeksteki fonksiyonu al ve çalıştır.
arr[3](); // merhaba
```
**Split kullanarak dizi oluşturmak**
Bir diziyi farklı şekillerde bölebilir ve diziyi değiştirebiliriz. Aşağıdaki örneklere bir göz atalım.
```jsx

let  js = 'JavaScript'

const  charsInJavaScript = js.split('')

  

console.log(charsInJavaScript) // ["J", "a", "v", "a", "S", "c", "r", "i", "p", "t"]

  

let  companiesString = 'Facebook, Google, Microsoft, Apple, IBM, Oracle, Amazon'

const  companies = companiesString.split(',')

  

console.log(companies) // ["Facebook", " Google", " Microsoft", " Apple", " IBM", " Oracle", " Amazon"]

let  txt =

'I love teaching and empowering people. I teach HTML, CSS, JS, React, Python.'

const  words = txt.split(' ')

  

console.log(words)

// metnin özel karakterleri var, sadece kelimeleri nasıl alabileceğinizi düşünün

// ["I", "love", "teaching", "and", "empowering", "people.", "I", "teach", "HTML,", "CSS,", "JS,", "React,", "Python"]

```
**index kullanarak dizi elemanlarına ulaşmak**
Dizide elemanların indexlerini kullanarak o elemana ulaşabiliriz. Dizinin index'i 0'dan başlar. Aşağıdaki örnek her elemanın indexini açıkça göstermektedir.
```jsx

const  numbers = [0, 3.14, 9.81, 37, 98.6, 100] // sayı dizisi

  

console.log(numbers.length) // => dizinin uzunluğunu bilebiliriz. O da 6'dır

console.log(numbers) // -> [0, 3.14, 9.81, 37, 98.6, 100]

console.log(numbers[0]) // -> 0

console.log(numbers[5]) // -> 100

  

let  lastIndex = numbers.length - 1;

console.log(numbers[lastIndex]) // -> 100

```





### **Dizileri manipüle edebilecek metotlar**

Diziyi manüple edebilmek için farklı metotlar vardır. Bunlar dizilerle uğraşmak için kullanışlı yöntemlerden bazılarıdır. Bu yöntemler: *Array, length, concat, indexOf, slice, splice, join, toString, includes, lastIndexOf, isArray, fill, push, pop, shift, unshift*

**Dizi Constructor**

Array:Bir dizi yaratmak için kullanılır.

```jsx


const  arr = Array() // boş bir dizi yaratır

console.log(arr)

  

const  eightEmptyValues = Array(8) // sekiz tane boş değer yaratır

console.log(eightEmptyValues) // [empty x 8]


```

**fill ile statik değerler yaratmak**

fill: Bütün dizi elemanlarını statik değerle doldurur.

```jsx

const  arr = Array() // Boş bir dizi yaratır

console.log(arr)

  

const  eightXvalues = Array(8).fill('X') // 'X'değerine sahip 8 tane eleman oluşuturur.

console.log(eightXvalues) // ['X', 'X','X','X','X','X','X','X']

  

const  eight0values = Array(8).fill(0) // '0' değerine sahip 8 tane eleman oluşturur.

console.log(eight0values) // [0, 0, 0, 0, 0, 0, 0, 0]

  

const  four4values = Array(4).fill(4) //'4' değerine sahip 8 tane eleman oluşturur.

console.log(four4values) // [4, 4, 4, 4]


```

**Concat kullanarak dizileri birleştirmek**

Concat sadece iki diziyi birleştirmez. ikiden fazla sayıda diziyi birleştirmenize izin verir.


```jsx

const  firstList = [1, 2, 3]

const  secondList = [4, 5, 6]

const  thirdList = firstList.concat(secondList)

  

console.log(thirdList) // [1, 2, 3, 4, 5, 6]

```

**Arr dizisinin içindeki indexe ulaşmak**

indexOf: O elemanın dizide olup olmadığını kontrol eder.Eğer o eleman dizide mevcutsa index numarasını, mevcut değilse -1 döner.


```jsx
const  numbers = [1, 2, 3, 4, 5]

  
console.log(numbers.indexOf(5)) // -> 4

console.log(numbers.indexOf(0)) // -> -1

console.log(numbers.indexOf(1)) // -> 0

console.log(numbers.indexOf(6)) // -> -1


//Listedeki elemanları kontrol edin.

// dizide bir banana olup olmadığını kontrol edelim

  
const  fruits = ['banana', 'orange', 'mango', 'lemon']

let  index = fruits.indexOf('banana') // 0

```

**Dizinin içindeki son indexe ulaşmak**

```jsx
const  numbers = [1, 2, 3, 4, 5, 3, 1, 2]

  

console.log(numbers.lastIndexOf(2)) // 7

console.log(numbers.lastIndexOf(0)) // -1

console.log(numbers.lastIndexOf(1)) // 6

console.log(numbers.lastIndexOf(4)) // 3

console.log(numbers.lastIndexOf(6)) // -1

```

**“includes” Bir dizide bir öğenin olup olmadığını kontrol etmek için kullanılır.Mevcut ise true değerini döndürür, aksi takdirde false değerini döndürür.**

```jsx
const  numbers = [1, 2, 3, 4, 5]

  
console.log(numbers.includes(5)) // true

console.log(numbers.includes(0)) // false

```

**Diziyi kontrol etmek**

“**Array.isArray**” Veri tipinin bir dizi olup olmadığını kontrol etmek için kullanılır.

```jsx
const  numbers = [1, 2, 3, 4, 5]

console.log(Array.isArray(numbers)) // true

```

**Diziyi stringe çevirmek**

```jsx
const  numbers = [1, 2, 3, 4, 5]

console.log(numbers.toString()) // 1,2,3,4,5

  
const  names = ['Asabeneh', 'Mathias', 'Elias', 'Brook']

console.log(names.toString()) // Asabeneh,Mathias,Elias,Brook

```

**Dizi elemanlarını Joinlemek**

“**join**” Dizinin elemanlarını birleştirmek için kullanılır, join yönteminde ilettiğimiz argüman dizide birleştirilir ve bir dizi olarak döndürülür. Varsayılan olarak bir virgül ile birleşir, ancak elemanlar arasında birleştirilebilecek farklı dizi parametreleri iletebiliriz.


```jsx
const  numbers = [1, 2, 3, 4, 5]

console.log(numbers.join()) // 1,2,3,4,5

  

const  names = ['Asabeneh', 'Mathias', 'Elias', 'Brook']

  

console.log(names.join()) // Asabeneh,Mathias,Elias,Brook

console.log(names.join('')) //AsabenehMathiasEliasBrook

console.log(names.join(' ')) //Asabeneh Mathias Elias Brook

console.log(names.join(', ')) //Asabeneh, Mathias, Elias, Brook

console.log(names.join(' # ')) //Asabeneh # Mathias # Elias # Brook

```

**Dizi elemanlarını “slice” etmek**

**“Slice”** Bir aralıktaki çoklu elemanları dilimler İki parametre alır. Bu parametreler, başlangıç ve bitiş konumlarıdır. Bitiş konumunu dahil etmez.


```jsx
const  numbers = [1,2,3,4,5]

console.log(numbers.slice()) // -> Bütün öğeyi kopyalar

console.log(numbers.slice(0)) // -> Bütün öğeyi kopyalar

console.log(numbers.slice(0, numbers.length)) // Bütün öğeyi kopyalar

console.log(numbers.slice(1,4)) // -> [2,3,4] // son elemanı dahil etmez

```

**Dizilerde splice metodu**

**“Splice”** üç parametre alır :başlangıç konumu, kaldırılması gereken eleman sayısı ve eklenmesi gereken eleman sayısı.




```jsx

const  numbers = [1, 2, 3, 4, 5]

numbers.splice()

console.log(numbers) // -> Bütün elemanları kaldırır

  

const  numbers = [1, 2, 3, 4, 5]

numbers.splice(0,1)

console.log(numbers) // ilk elemanı kaldırır



const  numbers = [1, 2, 3, 4, 5, 6]

numbers.splice(3, 3, 7, 8, 9)

console.log(numbers.splice(3, 3, 7, 8, 9)) // -> [1, 2, 3, 7, 8, 9] //2 eleman kaldırdı ve yerine 3 eleman ekledi


```

**Push kullanarak diziye eleman eklemek**

**“Push”** Dizinin sonuna eleman ekler.Varolan bir diziye eleman eklemek için push metodunu kullanırız.



```jsx
const  numbers = [1, 2, 3, 4, 5]

numbers.push(6)

console.log(numbers) // -> [1,2,3,4,5,6]

  

numbers.pop() // -> Dizinin sonundan bir eleman çıkarır.

console.log(numbers) // -> [1,2,3,4,5]

```

**pop kıllanarak diziden eleman çıkarmak**

**“pop”** Dizinin sonundaki elemanı siler.





```jsx
const  numbers = [1, 2, 3, 4, 5]

numbers.pop() // -> Sondaki elemanı siler

console.log(numbers) // -> [1,2,3,4]

```

**“Shift” Dizinin en başından eleman kaldırmak**

**“shift”** Dizinin en başındaki elemanı siler.



```jsx
const  numbers = [1, 2, 3, 4, 5]

numbers.shift() // -> baştan bir elemanı kaldırır.

console.log(numbers) // -> [2,3,4,5]

```

**“unshift” Dizinin en başına eleman eklemek**

**“unshift”** Dizinin başına dizi elemanı ekler.
```jsx
const  numbers = [1, 2, 3, 4, 5]

numbers.unshift(0) // -> en başa eleman ekler

console.log(numbers) // -> [0,1,2,3,4,5]

```

**“reverse” Dizi sırasını terse çevirmek**

reverse: Dizi sıralamasını terse çevirir.

```jsx
const  numbers = [1, 2, 3, 4, 5]

numbers.reverse() // -> ters dizi sırası

console.log(numbers) // [5, 4, 3, 2, 1]

  
numbers.reverse()

console.log(numbers) // [1, 2, 3, 4, 5]

```

**“sort” Dizi elemanlarını sıralamak**

**“sort”** Dizi elemanlarını alfabetik sırada düzenleyin.Sort call back fonksyonu alır, sort'un call back fonksiyonu ile nasıl kullandığımızı ilerleyen bölümlerde göreceğiz.


```jsx
const  webTechs = ['HTML', 'CSS', 'JavaScript', 'React', 'Redux', 'Node','MongoDB']

webTechs.sort()

console.log(webTechs) // ["CSS", "HTML", "JavaScript", "MongoDB", "Node", "React", "Redux"]

```