# Data Types (Veri Tipleri)

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

