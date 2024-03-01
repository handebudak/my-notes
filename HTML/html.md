
# TAGS

**1.Document Structure**

- <!DOCTYPE>
-  <html>
-  <head>
- <title>
-  <meta>
- <link>
-  <script>
- <noscript>

**2.Text Content**

-  <h1>, <h2>, <h3>, <h4>, <h5>, <h6>
-  <p>
-  <span>
-  <strong> : **`<strong>`** HTML etiketi, içeriğini vurgulamak için kullanılan bir içerik biçimlendirme etiketidir. Tarayıcılar bu etiketi kullanıcıya önemli olduğunu belirtmek için kullanır. Genellikle metin içeriğini kalın bir şekilde göstermek için kullanılır, ancak sadece biçimlendirme değil, içeriğin anlamı veya önemi üzerinde de vurgu yapar.
-  <em> :  HTML etiketi, içeriğini vurgulamak veya vurgulanmış bir parçayı vurgulamak için kullanılan bir içerik biçimlendirme etiketidir. Tarayıcılar bu etiketi kullanıcıya önemli olduğunu belirtmek için kullanır. Genellikle metin içeriğini italik bir şekilde göstermek için kullanılır, ancak sadece biçimlendirme değil, içeriğin anlamı veya önemi üzerinde de vurgu yapar.
-  <br> :  **`<br>`** HTML etiketi, bir satırın sonlandığını belirtmek için kullanılan bir içerik biçimlendirme etiketidir. "br" "line break" kelimesinin kısaltmasıdır ve bu etiket kullanıldığında bir sonraki içerik satırının bir alt satırdan başlayacağını belirtir.
-  <hr> :  Yatay bir çizgi veya yatay bir ayırıcı eklemek için kullanılan bir içerik biçimlendirme etiketidir. "hr" "horizontal rule" kelimesinin kısaltmasıdır. Bu etiket, içeriği iki parçaya bölmek veya belirli bir bölümü vurgulamak için kullanılır.

**3.Lists**

-  <ul>
-  <ol>
-  <li>
-  <dl> : (definition list) etiketi, tanımlı bir liste başlatır.
-  <dt> : (definition term) etiketi, bir terimi veya bir kavramı tanımlar.
- <dd> : (definition description) etiketi, bir terimin tanımını veya açıklamasını verir.

**4.Links and Navigation**

- <a>
- <nav>
- <link>

**5.Embedded Content**

- <img>
- <audio>
- <video>**
- <iframe>** : (inline frame) HTML içinde kullanılan bir etikettir ve başka bir web sayfasını veya içeriği içine gömme (embed) amacıyla kullanılır. `<iframe>` etiketi, içine aldığı kaynak belgesini (HTML, CSS, JavaScript vb.) bir çerçeve içinde görüntüler.

                     `<iframe>` etiketi, web sayfalarında farklı alanlar veya kaynaklar arasında iletişim kurmak, içerikleri gömmek veya harici içeriklerin görüntülenmesini sağlamak için kullanılabilir. Örneğin, harici bir web sitesinin içeriğini gömmek veya bir video oynatıcısı eklemek için kullanılabilir.

-  <canvas>
-  <svg> : SVG (Scalable Vector Graphics), HTML içinde kullanılan bir etikettir ve XML tabanlı bir dosya formatı olan SVG grafiklerini eklemek için kullanılır. SVG etiketi, web sayfalarında vektörel grafikler oluşturmak ve görüntülemek için kullanılır.

**6.Forms**

- <form>
- <input>
- <textarea>
- <button>
- <select>
- <option>
- <label> :  HTML etiketi, bir form elemanına (input, select, textarea gibi) eşlik eden açıklama veya etiketi tanımlamak için kullanılır. Kullanıcıya belirli bir form elemanının ne için olduğunu veya ne tür veri girmesi gerektiğini anlatmak için kullanılır. Bu, form elemanlarına daha iyi erişilebilirlik (accessibility) sağlar ve kullanıcı deneyimini iyileştirir.

```jsx
<label for="username">Kullanıcı Adı:</label>
<input type="text" id="username" name="username">

```

Bu örnekte, **`<label>`** etiketi "Kullanıcı Adı:" metnini tanımlar. **`for`** özelliği, bu etiketin hangi form elemanına bağlı olduğunu belirtir; burada **`for`** özelliği **`id="username"`** olan bir input alanına işaret eder. Bu sayede kullanıcılar "Kullanıcı Adı:" metnine tıkladığında, otomatik olarak ilgili input alanına odaklanır.

**`<label>`** etiketi, kullanıcı arayüzlerini daha erişilebilir hale getirmek için önemlidir. Özellikle ekran okuyucular gibi yardımcı teknolojilerle çalışan kullanıcılar için önemli bir işlevi vardır. Kullanıcıların form elemanlarını daha kolay anlamalarını ve kullanmalarını sağlar.

•  <fieldset> : **`<fieldset>`** HTML etiketi, bir formdaki ilişkili form elemanlarını gruplamak ve bunlara ortak bir çerçeve sağlamak için kullanılır. **`<fieldset>`** etiketi, form elemanlarını mantıksal olarak bir araya getirir ve bu gruplama işlemi, formun kullanıcılar için daha anlaşılır ve düzenli hale gelmesini sağlar.

                       **`<fieldset>`** etiketi genellikle **`<legend>`** etiketi ile birlikte kullanılır. **`<legend>`**, **`<fieldset>`** içindeki grup için bir başlık veya açıklama sağlar. Bu şekilde, kullanıcılar gruplanmış form elemanlarının ne hakkında olduğunu daha net bir şekilde anlayabilirler.

```jsx
<form>
  <fieldset>
    <legend>İletişim Bilgileri</legend>
    <label for="name">İsim:</label>
    <input type="text" id="name" name="name"><br>
    <label for="email">E-posta:</label>
    <input type="email" id="email" name="email"><br>
  </fieldset>
  <fieldset>
    <legend>Kargo Bilgileri</legend>
    <label for="address">Adres:</label>
    <input type="text" id="address" name="address"><br>
    <label for="city">Şehir:</label>
    <input type="text" id="city" name="city"><br>
  </fieldset>
  <input type="submit" value="Gönder">
</form>

```

**•  <legend>**
**•  <datalist> :**  **`<datalist>`**: Bu etiket, bir input alanına seçenekler sunmak için kullanılır. Kullanıcılar input alanına yazarken, bu seçenekler otomatik olarak gösterilir ve kullanıcının girişini tamamlamasına yardımcı olur. Özellikle, bir text input alanında kullanıcının bir öneri listesi arasından seçim yapmasını sağlamak için kullanılır.

```jsx
<label for="browser">Tarayıcı seçin:</label>
<input list="browsers" id="browser" name="browser">
<datalist id="browsers">
  <option value="Chrome">
  <option value="Firefox">
  <option value="Safari">
  <option value="Edge">
  <option value="Opera">
</datalist>

```

**•  <output> : `<output>`**: Bu etiket, bir formun sonucunu veya çıktısını göstermek için kullanılır. Özellikle, bir formun işlenmesinden sonra elde edilen sonuçları veya hesaplamaları göstermek için kullanılabilir. JavaScript kullanılarak form elemanlarının değerleri hesaplandığında veya değiştirildiğinde, bu değerlerin sonucunu **`<output>`** etiketi içinde gösterebilirsiniz.

```jsx
<form oninput="result.value = parseInt(x.value) + parseInt(y.value)">
  <input type="number" id="x" name="x" value="0"> +
  <input type="number" id="y" name="y" value="0"> =
  <output name="result" for="x y">0</output>
</form>

```

**7.Tables**

**•  <table>
•  <tr> : `<tr>`** (table row): Bu etiket, bir tablodaki bir satırı temsil eder. Tablodaki her satır, **`<tr>`** etiketi içinde yer alır.
**•  <th> : `<th>`** (table header): Bu etiket, bir tablonun başlık hücrelerini temsil eder. Başlık hücreleri genellikle tablonun sütunlarını tanımlar ve bold (kalın) metin ile gösterilir.
**•  <td> : `<td>`** (table data): Bu etiket, bir tablodaki veri hücrelerini temsil eder. Veri hücreleri, tablonun ana içeriğini oluşturur ve genellikle normal (yani, kalın olmayan) metin içerir.

```jsx
<table>
  <tr>
    <th>Adı</th>
    <th>Soyadı</th>
    <th>Yaşı</th>
  </tr>
  <tr>
    <td>Ahmet</td>
    <td>Yılmaz</td>
    <td>25</td>
  </tr>
  <tr>
    <td>Mehmet</td>
    <td>Demir</td>
    <td>30</td>
  </tr>
</table>

```

**•  <caption> :** Genel olarak, **`<caption>`** etiketi bir tablonun genel başlığını belirtmek için kullanılırken, **`<th>`** etiketi her bir sütunun başlığını belirtmek için kullanılır. **`<caption>`** etiketi tablonun içeriğine genel bir bakış sağlarken, **`<th>`** etiketi tablonun sütunlarını tanımlar ve her sütunun başlığını belirtir. Bu nedenle, hangi etiketin kullanılacağı, tablonun yapısına ve içeriğine bağlı olarak değişir.

```jsx
<table>
  <caption>Ürün Fiyatları</caption>
  <tr>
    <th>Ürün</th>
    <th>Fiyat</th>
  </tr>
  <tr>
    <td>Elma</td>
    <td>2 TL</td>
  </tr>
</table>

```

**8.Semantic Elements**

- <article>
- <section>
- <header>
- <footer>
-  <aside>
-  <main>
-  <figure> : Bu etiket, bir resim, diyagram, fotoğraf, çizim veya diğer görsel içeriği tanımlar. Genellikle, görsel içeriği bir **`<figure>`** etiketi içine yerleştirerek gruplandırırız. **`<figure>`** etiketi içine bir resim veya görsel içerikten başka metin veya açıklamalar da ekleyebiliriz.

```jsx
<figure>
  <img src="kedi.jpg" alt="Sevimli bir kedi">
  <figcaption>Sevimli bir kedi</figcaption>
</figure>

```

- <figcaption>
- <mark> :  HTML etiketi, belirli bir metin parçasını vurgulamak için kullanılır. Bu etiket, belirli bir metin parçasını sararak veya arka planını değiştirerek vurgulama efekti sağlar. 

                    Tarayıcılar,   **`<mark>`** etiketini gördüklerinde, içine aldığı metni genellikle sarı bir arka planla vurgularlar, ancak CSS kullanarak bu görünümü değiştirebilirsiniz.

```jsx
<p>Çok önemli bir <mark>not</mark> eklemem gerekiyor.</p>

```

- <progress> :  HTML etiketi, bir işlemin yüzde oranını veya ilerleme durumunu göstermek için kullanılır. Özellikle, bir formun işlenmesi veya bir dosyanın yüklenmesi gibi süreçlerde kullanıcıya ilerleme durumunu göstermek için yaygın olarak kullanılır.

                           **`<progress>`** etiketi, bir doluluk çubuğu veya ilerleme çubuğu olarak tarayıcılar tarafından render edilir. Bu çubuk, işlemin tamamlanma yüzdesini veya ilerleme durumunu gösterir. Özellikle, **`value`** ve **`max`** özellikleri kullanılarak belirli bir işlemin tamamlanma yüzdesi belirtilir.

```jsx
<label for="file">Dosya Yükleme:</label>
<progress id="file" value="50" max="100"></progress>

```

Bu örnekte, **`<progress>`** etiketi ile bir dosya yükleme işleminin yüzde oranını göstermek için kullanılmıştır. **`value`** özelliği ile mevcut ilerleme yüzdesi (burada %50), **`max`** özelliği ile ise tamamlanma yüzdesinin maksimum değeri (yani, %100) belirtilmiştir.

**`<progress>`** etiketi, kullanıcıların belirli bir işlemin ne kadarının tamamlandığını açıkça görmelerini sağlar ve bu da kullanıcı deneyimini iyileştirir. Özellikle, uzun süren işlemlerde veya dosya yükleme gibi işlemlerde kullanıcıya ilerleme durumunu göstermek için önemlidir.

- <time> : Belirli bir tarihi veya zamanı tanımlamak için kullanılır. Bu etiket, belirli bir zamanı insanlar tarafından okunabilir ve makine tarafından işlenebilir bir formatta gösterir.

                  **`<time>`** etiketi, iki önemli özelliğe sahiptir:

1. **`datetime`** özelliği: Bu özellik, belirli bir tarihi veya zamanı ISO 8601 formatında tanımlar. ISO 8601 formatı, yıl-ay-gün saat:dakika:saniye formatında (YYYY-MM-DDTHH:MM:SS) ve zaman dilimi bilgisi içerir. Bu format, makine tarafından işlenebilir ve uluslararası standartlara uygundur.
2. İçerik: **`<time>`** etiketinin içeriği, kullanıcılar için okunabilir bir metin biçiminde belirli bir tarihi veya zamanı temsil eder. Bu, kullanıcıların belirli bir tarihi veya zamanı daha kolay anlamalarını sağlar.

```jsx
<p>Maç tarihi: <time datetime="2024-03-01T19:00:00">1 Mart 2024, 19:00</time></p>

```

Bu örnekte, **`<time>`** etiketi ile bir maçın başlama tarihini ve saati tanımlanmıştır. **`datetime`** özelliği ile belirli bir tarih ve zaman ISO 8601 formatında belirtilmiştir. Etiketin içeriği ise insanlar için okunabilir bir biçimde maçın başlama tarihini ve saati temsil eder.

**`<time>`** etiketi, web sayfalarında belirli bir tarihi veya zamanı açıkça tanımlamak ve bu bilginin hem insanlar hem de makineler tarafından anlaşılabilir olmasını sağlamak için önemlidir.

- <details> : `<details>`** HTML elementi, kullanıcıların bir içeriği açıp kapatabileceği, genişletilebilir bir bilgi kutusunu temsil eder. Bu element, kullanıcılara bir konuyu özetleyen başlık veya etiket ile birlikte bir içeriği gizlemek ve açmak için kullanılır.

                      **`<details>`** elementi genellikle **`<summary>`** elementi ile birlikte kullanılır.

**•  <summary>: `<summary>`**, kullanıcıların tıkladığında detayları görebileceği bir başlık veya açılır menüyü temsil eder. **`<details>`** elementi ise bu başlığın altında gizlenmiş olan detaylı içeriği barındırır.

```jsx
<details>
  <summary>Detayları Gör</summary>
  <p>Burada detaylı açıklamalar yer alabilir.</p>
</details>

```

Bu örnekte, **`<details>`** elementi ile bir detaylar kutusu oluşturulmuştur. Kullanıcılar "Detayları Gör" başlığına tıkladıklarında, **`<p>`** elementi içindeki detaylı açıklamaların görünürlüğü değişir. Varsayılan olarak, detaylar gizlidir, ancak kullanıcılar tıkladıklarında açılabilir. Bu, daha fazla bilgi sunmak için kullanışlı bir yol olabilir ve genellikle sıkça sorulan sorular (SSS) veya kullanım koşulları gibi içeriklerde kullanılır.


**9.Deprecated Elements (Avoid Using)**

- <center>
- <font>
- <strike>**

