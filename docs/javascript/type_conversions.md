# Type Conversions (Tip Dönüşümleri)

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