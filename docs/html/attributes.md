# Attributes

## accesskey

**`accesskey`**

Geçerli öğe için klavye kısayolu oluşturmaya yönelik bir ipucu sağlar. Bu özellik boşlukla ayrılmış bir karakter listesinden oluşur. Tarayıcı, bilgisayar klavye düzeninde bulunan ilk düzeni kullanmalıdır.

**`accesskey`**, HTML içindeki bir form elemanına klavye kısayolu atamak için kullanılan bir özelliktir. Bu özellik, kullanıcıların klavye kullanarak belirli bir form elemanına hızlıca erişmelerini sağlar. Kullanıcılar, belirtilen klavye kısayolunu kullanarak form elemanına odaklanabilir ve gerekli eylemi gerçekleştirebilirler.

**`accesskey`** özelliği, bir form elemanına bir harf atanarak belirtilir. Kullanıcılar, bu harfi kullanarak form elemanına erişebilirler. Örneğin, bir form içindeki bir metin giriş alanına erişmek için klavyede "Alt" tuşuna basılırken aynı zamanda "M" harfine basmak gibi.

```html
<label for="search">Arama:</label>
<input type="text" id="search" name="search" accesskey="s" />
```

## autocapitalize

**`autocapitalize`** HTML özelliği, bir metin giriş alanının otomatik olarak büyük harfle başlamasını veya büyük harfe dönüştürülmesini sağlayan bir özelliktir. Bu özellik, kullanıcıların bir metin giriş alanına girdikleri metinlerin otomatik olarak büyük harfle başlamasını veya belirli bir metni büyük harfe dönüştürmesini kolaylaştırmak için kullanılır.

**`autocapitalize`** özelliği, aşağıdaki değerlerden birini alabilir:

- **`none`**: Metnin otomatik olarak büyük harfle başlamamasını belirtir.
- **`words`**: Her kelimenin baş harfinin otomatik olarak büyük harfle başlamasını belirtir.
- **`sentences`**: Her cümlenin baş harfinin otomatik olarak büyük harfle başlamasını belirtir.
- **`characters`**: Her karakterin otomatik olarak büyük harfe dönüştürülmesini belirtir.

```html
<input type="text" autocapitalize="words" />
```

## autofocus

**`autofocus`** HTML özelliği, bir sayfa yüklendiğinde veya bir form elemanı görüntülendiğinde, o elemana otomatik olarak odaklanılmasını sağlar. Bu özellik, sayfa yüklendiğinde veya form elemanı görüntülendiğinde kullanıcının doğrudan o elemana giriş yapmasını kolaylaştırır.

Örneğin, bir sayfa yüklendiğinde bir metin giriş alanına otomatik olarak odaklanılmasını istiyorsanız, **`autofocus`** özelliğini kullanabilirsiniz.

```html
<input type="text" autofocus />
```

## contenteditable

**`contenteditable`**

Öğenin kullanıcı tarafından düzenlenebilmesi gerekip gerekmediğini belirten [numaralandırılmış](https://developer.mozilla.org/en-US/docs/Glossary/Enumerated) bir özellik. Böyle bir durumda tarayıcı, düzenlemeye izin verecek şekilde widget'ını değiştirir. Özellik aşağıdaki değerlerden birini almalıdır:
• `true`veya öğenin düzenlenebilir olması gerektiğini belirten *boş dize ;*
• `false`Bu, öğenin düzenlenemez olması gerektiğini belirtir.

```html
<table contenteditable="true"></table>
```

## contextmenu

**`contextmenu`** HTML özelliği, bir elementin üzerine sağ tıklandığında görüntülenecek olan bağlam menüsünü belirlemek için kullanılır. Bu özellik, bir elementin üzerine sağ tıklandığında kullanıcıya sunulan seçenekleri kontrol etmek için kullanılır.

Bağlam menüsü, kullanıcının bir web sayfasında bir element üzerinde sağ tıkladığında açılan ve o elementle ilgili seçenekleri içeren küçük bir menüdür. Bu menü, özelleştirilmiş veya önceden tanımlanmış seçenekler içerebilir. Örneğin, bir resim üzerinde sağ tıklandığında "Resmi Kaydet", "Resmi Aç", "Resmi Kopyala" gibi seçenekler içeren bir bağlam menüsü görünebilir.

**`contextmenu`** özelliği, bir elementin üzerine sağ tıklandığında hangi bağlam menüsünün görüntüleneceğini belirler. Bu özellik, bir bağlam menüsü oluşturmak ve özelleştirmek için bir **`<menu>`** elementine referans verir.

```html
<img src="resim.png" contextmenu="resim-menu" />
<menu type="context" id="resim-menu">
  <menuitem label="Resmi Kaydet"></menuitem>
  <menuitem label="Resmi Aç"></menuitem>
  <menuitem label="Resmi Kopyala"></menuitem>
</menu>
```

## data

**`data-*`** özelliği, HTML elementlerine özel veri öznitelikleri eklemek için kullanılır. Bu özellik, HTML elementlerine ekstra bilgi veya özellikler eklemek ve bu bilgiyi JavaScript gibi istemci tarafı kodlama ortamlarında kullanmak için kullanılır. Özel veri öznitelikleri, **`data-`** ile başlayan herhangi bir isme sahip olabilir ve elemente bağlı özel veri sağlar.

Özel veri öznitelikleri, genellikle bir elementin üzerinde daha fazla bilgi saklamak, belirli bir işlevi etkinleştirmek veya elementin belirli bir durumunu temsil etmek için kullanılır. Bu veriler, JavaScript kodu tarafından alınabilir ve işlenebilir.

```html
<div id="ürün" data-id="12345" data-ad="Telefon" data-fiyat="1500"></div>
```

Bu örnekte, bir '< div>' elementine ürünle ilgili ekstra bilgiler eklenmiştir. data-id, data-ad ve data-fiyat gibi özel veri öznitelikleri, bu ürüne ilişkin benzersiz bir kimlik, ad ve fiyat bilgilerini temsil eder. JavaScript kodu, bu özelliklere erişerek ve bunları işleyerek bu ekstra bilgileri kullanabilir. Örneğin, bir alışveriş sepeti uygulamasında kullanıcı bu ürünü sepete eklediğinde, bu özelliklerden faydalanılabilir ve ürünün kimliği, adı ve fiyatı gibi bilgileri işlemek için kullanılabilir.

## dir

**`dir`** HTML özelliği, bir elementin içeriğinin ve metnin yazı yönünü belirtmek için kullanılır. Bu özellik, özellikle sağdan sola yazılan dillerle yazılan metinlerin doğru bir şekilde görüntülenmesini sağlamak için kullanılır.

**`dir`** özelliği, aşağıdaki değerlerden birini alabilir:

- **`ltr`**: Metnin soldan sağa doğru yazılmasını belirtir. Bu değer, tipik olarak soldan sağa yazılan diller (İngilizce, Türkçe, vb.) için kullanılır.
- **`rtl`**: Metnin sağdan sola doğru yazılmasını belirtir. Bu değer, sağdan sola yazılan diller (Arapça, Farsça, vb.) için kullanılır.

Örneğin, bir metin kutusunda Arapça bir metin göstermek istiyorsanız, metin kutusuna **`dir="rtl"`** özelliğini ekleyerek metnin sağdan sola doğru gösterilmesini sağlayabilirsiniz.

```html
<input type="text" value="مرحبا" dir="rtl" />
```

## draggable

**`draggable`**, HTML özelliği, bir elementin sürüklenebilir olup olmadığını belirtmek için kullanılır. Bu özellik, özellikle web uygulamalarında sürükleyip bırakma işlevselliği sağlamak için kullanılır.

Bir elementin **`draggable`** özelliği varsayılan olarak **`false`** değerindedir. Ancak, bu özelliği **`true`** olarak ayarlayarak bir elementin sürüklenebilir hale gelmesini sağlayabilirsiniz.

```html
<div draggable="true">Bu bir sürüklenebilir elementtir.</div>
```

## enterkeyhint

**`enterkeyhint`**, HTML özelliği, bir metin giriş alanında kullanıcının Enter tuşuna basıldığında hangi eylemin gerçekleştirileceğini belirtmek için kullanılır. Bu özellik, kullanıcı deneyimini iyileştirmek ve doğru klavye davranışını sağlamak için kullanılır.

**`enterkeyhint`** özelliği aşağıdaki değerlerden birini alabilir:

- **`"enter"`**: Metin giriş alanında Enter tuşuna basıldığında, genellikle bir formun gönderilmesi gibi bir eylem gerçekleştirileceğini belirtir.
- **`"done"`**: Metin giriş alanında Enter tuşuna basıldığında, genellikle bir işlemi tamamlama veya bir işlemi bitirme gibi bir eylem gerçekleştirileceğini belirtir.
- **`"go"`**: Metin giriş alanında Enter tuşuna basıldığında, genellikle bir URL'ye gitme veya bir sayfayı yükleme gibi bir eylem gerçekleştirileceğini belirtir.
- **`"next"`**: Metin giriş alanında Enter tuşuna basıldığında, genellikle bir sonraki alana geçme veya bir sonraki adıma geçme gibi bir eylem gerçekleştirileceğini belirtir.
- **`"search"`**: Metin giriş alanında Enter tuşuna basıldığında, genellikle bir arama sorgusu gönderme veya arama sonuçlarını gösterme gibi bir eylem gerçekleştirileceğini belirtir.
- **`"send"`**: Metin giriş alanında Enter tuşuna basıldığında, genellikle bir mesajı gönderme veya iletişim formunu gönderme gibi bir eylem gerçekleştirileceğini belirtir.

```html
<input type="text" enterkeyhint="search" />
```

## exportparts

**`exportparts`**, bir HTML öğesinde bulunan iç alt öğelerin, dışarıya ihraç edilebilecek veya başka bir deyişle dışarıya aktarılabilecek bir parçasını belirlemek için kullanılan bir özelliktir. Bu özellik, web bileşenlerinin (web components) içeriğini ve stilini dış dünyayla paylaşmak için kullanılır.

**`exportparts`** özelliği, bir bileşenin iç alt öğelerinin birbirinden ayrı olarak kullanılabilmesini sağlar. Böylece, bileşenin dışındaki kodlar, iç alt öğelerin stillerini veya işlevlerini doğrudan kontrol edebilir.

```html
<my-custom-element exportparts="part1, part2">
  <div id="part1">İçerik 1</div>
  <div id="part2">İçerik 2</div>
</my-custom-element>
```

## hidden

**`hidden`**, HTML özelliği bir elementin görünürlüğünü kontrol etmek için kullanılır. Bu özellik, bir elementin görünür veya gizli olmasını sağlar.

Bir elementin **`hidden`** özelliği eklenirse, tarayıcı bu elementi sayfa üzerinde gizler ve görünmez hale getirir. Ancak, element sayfa kaynağında hala var olur ve DOM'da yer alır. Yani, tarayıcı bu elementi sadece ekranda göstermez, ancak sayfa yapıları içinde hala mevcuttur.

## inert

**`inert`** HTML özelliği, bir elementin ve alt elemanlarının etkileşime kapalı olmasını sağlar. Bu özellik, bir elementin üzerindeki tüm etkileşimleri devre dışı bırakır, böylece kullanıcılar bu element üzerinde tıklama yapamaz veya içeriğini değiştiremez.

**`inert`** özelliği, bir elementin etkileşim dışı olmasını sağlamak için kullanılırken, aynı zamanda bu elementin içeriğinin tarayıcı tarafından işlenmemesini sağlar. Bu, ekran okuyucular veya klavye gezinimi gibi erişilebilirlik araçları tarafından içeriğin atlanmasını sağlar.

```html
<div inert>
  Bu içerik etkileşime kapalıdır.
  <button>Tıklanabilir Düğme</button>
</div>
```

## inputmode

**`inputmode`**, HTML özelliği bir giriş alanındaki kullanıcının hangi tür klavye düzeninin kullanılacağını belirtmek için kullanılır. Bu özellik, kullanıcının hangi tür veri girişi yapacağını daha doğru bir şekilde belirtmek için kullanılır ve tarayıcıya kullanıcı arayüzünü uygun şekilde ayarlama konusunda ipucu verir.

**`inputmode`** özelliği, aşağıdaki değerlerden birini alabilir:

- **`none`**: Özel bir giriş modu belirtilmez. Bu, varsayılan klavye düzeninin kullanılmasını sağlar.
- **`text`**: Metin girişi yapılacağını belirtir.
- **`tel`**: Telefon numarası girişi yapılacağını belirtir.
- **`url`**: URL girişi yapılacağını belirtir.
- **`email`**: E-posta adresi girişi yapılacağını belirtir.
- **`numeric`**: Sayısal giriş yapılacağını belirtir.
- **`decimal`**: Ondalıklı sayı girişi yapılacağını belirtir.
- **`search`**: Arama sorgusu girişi yapılacağını belirtir.

```html
<input type="text" inputmode="numeric" />
```

## is

**`is`**, HTML özelliği, bir elementin belirli bir türde bir özelleştirilmiş öğe olduğunu belirtmek için kullanılır. Bu özellik, özellikle Web Components gibi özelleştirilmiş bileşenler oluştururken ve bu bileşenlerin belirli bir türde bir HTML elementi olduğunu belirtirken kullanılır.

Örneğin, bir özel element oluştururken, bu elementin bir düğme olduğunu belirtmek için **`is`** özelliği kullanılabilir. Bu, tarayıcıya bu özel elementin bir düğme gibi davranması gerektiğini söyler.

```
<button is="my-custom-button">
Özel Düğme
</button>
```

Bu örnekte, bir **`<button>`** elementi oluşturulurken **`is`** özelliği ile **`my-custom-button`** değeri atanmıştır. Bu, bu düğmenin özel bir düğme olduğunu belirtir. **`my-custom-button`** adındaki özel bir bileşenin bu düğmeye uygulanacağını ve bu bileşenin davranışını ve görünümünü etkileyeceğini belirtir.

**`is`** özelliği, özellikle Web Components ve özelleştirilmiş bileşenlerle çalışırken kullanışlıdır. Bu, HTML elementlerine özel davranışlar ve özellikler eklemek için yaygın olarak kullanılan bir tekniktir. Ancak, **`is`** özelliğinin kullanımı, tarayıcı uyumluluğunu dikkate almak ve dikkatli bir şekilde yapılmalıdır, çünkü tüm tarayıcılar bu özelliği desteklemeyebilir.

## itemid

**`itemid`** HTML özelliği, bir HTML elementinin bir öğe veya nesne ile ilişkilendirildiği bir kimlik (ID) değerini belirtmek için kullanılır. Bu özellik, öğenin benzersiz bir kimliğe sahip olduğunu ve bu kimliğin belirli bir nesneye atandığını belirtir.

**`itemid`** özelliği, genellikle bir HTML belgesindeki farklı öğeler arasındaki ilişkileri belirtmek için kullanılır. Örneğin, bir web sayfasında bir haber makalesi ve bu makaleye ait yorumlar varsa, her yorum öğesine, yorumun makaleyle ilişkilendirildiğini belirtmek için **`itemid`** özelliği atanabilir.

```html
<article itemid="https://example.com/article123">
  <h1>Article Title</h1>
  <p>Article content...</p>
</article>
```

Bu örnekte, bir **`<article>`** elementi oluşturulurken **`itemid`** özelliği ile bir URL değeri atanmıştır. Bu, bu makalenin bir kimliğe sahip olduğunu ve bu kimliğin **`https://example.com/article123`** olduğunu belirtir. Bu, makalenin belirli bir öğeyle ilişkilendirildiğini ve diğer sayfalarda bu öğe ile ilişkilendirme yapmak için bu kimliği kullanabileceğimizi gösterir.

**`itemid`** özelliği, genellikle Semantic Web ve veri bağlantılı web siteleri gibi bağlamda yaygın olarak kullanılır. Ancak, genel web sayfalarında da kullanılabilir ve belirli bir öğenin benzersiz bir kimliğe sahip olduğunu belirtmek için kullanışlı olabilir.

## itemprop

**`itemprop`**, HTML özelliği, mikro veri (microdata) özelliğidir ve bir HTML elementinin belirli bir özelliği temsil ettiğini belirtmek için kullanılır. Bu özellik, web sayfalarındaki içeriği makine tarafından daha iyi anlaşılır hale getirmek için kullanılır.

**`itemprop`** özelliği, bir HTML öğesinin içeriğinin bir nesne veya özellikle ilişkilendirilmesini sağlar. Örneğin, bir **`<span>`** öğesinde bir kişinin adını temsil ediyorsa, **`itemprop`** özelliği ile "name" gibi bir özelliğe işaret edilebilir.

```html
<p>Benim adım <span itemprop="name">John Doe</span></p>
```

Bu örnekte, bir **`<span>`** öğesi oluşturulmuş ve içeriğinin bir kişinin adını temsil ettiği belirtilmiştir. **`itemprop="name"`** özelliği, bu **`<span>`** öğesinin "name" özelliğini temsil ettiğini ve içeriğinin bir kişinin adını içerdiğini belirtir.

**`itemprop`** özelliği, web sayfalarında yapısal veri (structured data) oluşturmak ve bu verilerin arama motorları ve diğer veri analizi araçları tarafından daha iyi anlaşılmasını sağlamak için kullanılır. Bu, arama sonuçlarının zenginleştirilmesine, kullanıcı deneyiminin iyileştirilmesine ve arama motoru optimizasyonuna (SEO) katkıda bulunur.

## itemref

**`itemref`**, HTML özelliği, bir elementin diğer mikro veri (microdata) öğelerine referans verdiğini belirtmek için kullanılır. Bu özellik, bir elementin mikro veri öğeleri arasında ilişki kurmasına olanak tanır.

**`itemref`** özelliği, bir HTML elementinin mikro veri öğeleri arasındaki ilişkileri açıklamak için kullanılır. Özellikle, bir elementin kendi içeriğindeki veriyi tam olarak temsil etmediği durumlarda, bu elementin diğer öğelere referans vermesine izin verir.

```html
<div itemscope itemtype="http://schema.org/Person" id="person">
  <p>
    Adı: <span itemprop="name">John Doe</span><br />
    Yaşı: <span itemprop="age">30</span><br />
    Doğum yeri: <span itemprop="birthPlace" itemref="city">Unknown</span>
  </p>
</div>

<div id="city" itemscope itemtype="http://schema.org/City">
  <span itemprop="name">New York</span>
</div>
```

Bu örnekte, bir kişi ve bir şehirle ilgili mikro veri oluşturulmuştur. **`<div id="person">`** içindeki kişi öğesi, **`itemref`** özelliğiyle **`<div id="city">`** öğesine referans verir. Böylece, kişinin doğum yeri bilgisine bağlı olarak **`itemref`** özelliği, **`city`** öğesine referans verir. Bu, doğum yeri bilgisinin **`City`** tipindeki mikro veriye sahip olan **`city`** öğesinden alındığını gösterir.

**`itemref`**, mikro veri oluştururken karmaşık veri yapılarını tanımlamak ve ilişkileri açıklamak için kullanılır. Bu, web sayfalarındaki yapısal verinin daha anlaşılır hale getirilmesine yardımcı olur ve arama motorlarının içeriği daha doğru bir şekilde anlamasına olanak tanır.

## itemscope

**`itemscope`**, HTML özelliği, bir elementin mikro veri (microdata) öğesi olduğunu belirtmek için kullanılır. Bu özellik, web sayfalarında yapısal veri eklemek için kullanılan bir mikro veri özelliğidir.

Bir elementin **`itemscope`** özelliği ile işaretlenmesi, bu elementin içeriğinin bir nesneyi veya öğeyi temsil ettiğini belirtir. Bu nesne veya öğe genellikle bir şeyin tanımını veya bir özelliğini ifade eder.

**`itemscope`** özelliği, bir HTML elementinin başka bir elementin bir parçası olduğunu belirten **`itemprop`** özellikleriyle birlikte kullanılır. Bu sayede, web tarayıcıları ve diğer arama motorları, bu öğenin içeriğini daha iyi anlayabilir ve yapısal veriyi daha etkili bir şekilde işleyebilir.

```html
<div itemscope>
  <p>
    Benim adım <span itemprop="name">John Doe</span> ve ben
    <span itemprop="jobTitle">yazılım geliştiriciyim</span>.
  </p>
</div>
```

Bu örnekte, bir < div> elementi oluşturulurken itemscope özelliği eklenmiştir. Bu, < div> elementinin bir mikro veri öğesi olduğunu belirtir. İçeriği, bir kişinin adını (name) ve mesleğini (jobTitle) temsil eden < span> öğeleriyle tanımlanmıştır. Bu mikro veri öğeleri, yapısal veriyi temsil eder ve web tarayıcılarına ve arama motorlarına bu içeriği daha iyi anlamaları için ipuçları sağlar.

## itemtype

**`itemtype`**, HTML özelliği, bir elementin içeriğinin bir mikro veri türünü temsil ettiğini belirtmek için kullanılır. Bu özellik, mikro veri (microdata) yapılandırma dilinde bir elementin hangi türde bir veriyi temsil ettiğini tanımlamak için kullanılır.

**`itemtype`** özelliği, bir elementin içeriğinin bir mikro veri türü olduğunu belirtir ve genellikle **`schema.org`** gibi bir mikro veri türü tanımlama kaynağına (vocabulary) bir URL ile atıfta bulunur.

```html
<div itemscope itemtype="http://schema.org/Person">
  <span itemprop="name">John Doe</span>
</div>
```

Bu örnekte, bir **`<div>`** elementi oluşturulurken **`itemscope`** ve **`itemtype`** özellikleri eklenmiştir. **`itemtype`** özelliği, bu **`<div>`** elementinin bir mikro veri türü olan "Person" (Kişi) türünü temsil ettiğini belirtir. Bu, içerideki verinin bir kişiyi tanımladığını ve **`schema.org`** gibi bir kaynağa göre yapılandırıldığını gösterir.

**`itemtype`** özelliği, web sayfalarında yapısal veriyi belirlemek ve arama motorlarına içeriği daha iyi anlatmak için kullanılır. Bu özellik, yapısal verinin daha doğru bir şekilde anlaşılmasına ve arama sonuçlarının zenginleştirilmesine katkıda bulunur.

## nonce

**`nonce`**, HTML içindeki **`<script>`** ve **`<style>`** etiketlerinin güvenliğini artırmak için kullanılan bir özelliktir. "nonce" kelimesi "number used once" (bir kez kullanılan sayı) kısaltmasıdır. Bu, tarayıcının belirli bir **`<script>`** veya **`<style>`** etiketinin içeriğinin yalnızca belirli bir sayısal değere sahip bir "nonce" ile eşleştiğini doğrulamasını sağlar.

Bir "nonce" değeri, sunucu tarafından dinamik olarak oluşturulur ve HTML sayfasına eklenir. Bu değer, her sayfa yüklendiğinde veya her istek yapıldığında değişebilir. Tarayıcı, bir **`<script>`** veya **`<style>`** etiketinin içeriğini çalıştırmadan önce, bu etiketin **`nonce`** özelliği ile belirtilen "nonce" değerini kontrol eder. Eğer bu "nonce" değeri ile eşleşmiyorsa, içerik çalıştırılmaz veya uygulanmaz.

Bu yöntem, XSS (Cross-Site Scripting) saldırılarını önlemeye yardımcı olur. XSS saldırıları, kötü niyetli kullanıcıların web uygulamalarına zararlı JavaScript kodlarını enjekte etmelerini sağlar. **`nonce`** özelliği, tarayıcının yalnızca doğru **`nonce`** değerine sahip olan **`<script>`** veya **`<style>`** etiketlerini çalıştırmasını sağlayarak, bu tür saldırıları engeller.

```html
<script nonce="abc123">
  console.log("Bu script doğru nonce değeriyle çalışacak.");
</script>
```

Bu örnekte, < script> etiketi içinde nonce özelliği belirtilmiştir ve değeri abc123 olarak ayarlanmıştır. Bu, tarayıcının bu < script> etiketinin içeriğini yalnızca nonce değeri abc123 ile eşleşen bir etiket olduğunda çalıştırmasını sağlar.

## part

**Part**", CSS'de bir elementin içeriğinin veya davranışının dış dünyaya aktarılabilecek bağımsız bir parçasını ifade eder. Bu kavram, özellikle web bileşenleri (web components) ve özelleştirilmiş bileşenlerin oluşturulmasında önemlidir.

Bir HTML elementinin belirli bir parçasını dışarıya aktarmak için **`::part()`** pseudo-elementi kullanılır. Bu, elementin içindeki belirli bir bölümü stillemek veya etkileşim eklemek için kullanışlıdır. Bu yöntem, bir bileşenin iç yapısının değişmesi durumunda bile dış dünyadaki kullanımların etkilenmemesini sağlar.

Örneğin, bir buton bileşeni oluştururken, bu butonun içindeki metni veya simgeleri dış dünyaya aktarmak için "part" adını verdiğimiz bölümler oluşturabiliriz. Böylece, bu butonu kullanan geliştiriciler veya tasarımcılar, içerideki parçaları özelleştirebilir veya stilleyebilirler.

```html
<button class="custom-button">
  <span class="label">Click Me</span>
  <span class="icon">🚀</span>
</button>
```

```css
.custom-button::part(label) {
  font-weight: bold;
}
.custom-button::part(icon) {
  margin-left: 5px;
}
```

Bu örnekte, bir buton bileşeni oluşturulmuş ve içinde "label" ve "icon" adında iki ayrı parça tanımlanmıştır. CSS'de bu parçalara ::part() pseudo-elementi ile erişilmiş ve özel stiller eklenmiştir. Bu, buton bileşenini kullanırken içerideki parçaları özelleştirmenin kolay ve esnek bir yolunu sağlar.

## popover

"**Popover**", web geliştirme ve kullanıcı arayüzü tasarımında yaygın olarak kullanılan bir terimdir. Genellikle kullanıcıya bir mesaj, bilgi veya seçenekler sunmak için kullanılan bir arayüz öğesidir. Popover'lar genellikle bir kullanıcı bir öğenin üzerine gelince veya bir düğmeye tıkladığında görüntülenir ve kullanıcının işlem yapmasına veya daha fazla bilgi edinmesine olanak tanır.

Popüler web arayüz kütüphaneleri ve çerçeveleri, önceden oluşturulmuş popover bileşenleri sağlarlar ve bu bileşenleri kolayca projelere entegre etmeye olanak tanır. Popover'lar genellikle CSS, JavaScript ve HTML kullanılarak özelleştirilebilir ve belirli bir projenin gereksinimlerine göre uyarlanabilir.

Bir popover, kullanıcıya bir ipucu, uyarı mesajı, seçenekler menüsü veya daha fazla ayrıntı gibi çeşitli içerikler sunabilir. Örneğin, bir kullanıcı bir düğmeye fareyi getirdiğinde veya üzerine tıkladığında, bu düğmeye ilişkin ek bilgiler veya seçenekler içeren bir popover görünebilir.

Popover'lar, kullanıcı arayüzünü zenginleştirmek, kullanıcı deneyimini geliştirmek ve kullanıcıların daha iyi bilgilendirilmesini sağlamak için yaygın olarak kullanılır. İyi tasarlanmış bir popover, kullanıcıların belirli bir işlemi daha kolay ve hızlı bir şekilde gerçekleştirmelerine yardımcı olabilir.

## role

"**role**", HTML'de kullanılan bir özelliktir ve bir HTML elementinin belirli bir rolü veya işlevi olduğunu belirtmek için kullanılır. Bu özellik, özellikle erişilebilirlik (accessibility) için önemlidir ve tarayıcılara ve ekran okuyuculara bir elementin kullanım amacını anlatmak için kullanılır.

"role" özelliği, bir elementin davranışını ve etkileşimini açıklamak için kullanılır. Örneğin, bir düğme bir düğme olduğunu belirtmek için "role" özelliği kullanılabilir. Böylece, ekran okuyucular gibi erişilebilirlik araçları, kullanıcılara bu düğmenin bir işlemi tetikleyebileceğini söyleyebilir.

```html
<button role="button">Tıkla!</button>
```

Bu örnekte, bir **`<button>`** elementi oluşturulurken "role" özelliği ile "button" rolü atanmıştır. Bu, bu elementin bir düğme olduğunu belirtir. Tarayıcılar ve ekran okuyucular, bu elementin bir düğme olduğunu ve tıklanabilir bir işlemi temsil ettiğini bilir ve kullanıcılara bu şekilde bildirir.

"role" özelliği, özellikle özelleştirilmiş veya karmaşık bileşenler oluşturulurken, HTML'de standart bir elementin kullanım amacını açıklamakta yetersiz kalındığında kullanışlıdır. Bu, erişilebilirlik ve kullanıcı deneyimi açısından önemlidir, çünkü doğru bir şekilde belirtilmiş roller, kullanıcıların web sayfalarıyla daha iyi etkileşimde bulunmasına yardımcı olur.

## slot

"**Slot"**, HTML içinde özelleştirilmiş veya yeniden kullanılabilir bileşenlerin geliştirilmesinde ve kullanılmasında önemli bir kavramdır. Web bileşenlerinin (web components) bir parçası olan "slot", bir bileşenin içeriğini dışarıdan almasını veya değişken içeriğe sahip olmasını sağlar.

Slotlar, bir bileşenin içinde belirli bir alanı işaret etmek için kullanılır. Bu alan, bileşenin kullanıldığı yerde farklı içeriklerin yerleştirilmesine izin verir. Böylece, bir bileşenin içindeki içeriğin dışarıdan değiştirilebilmesi veya özelleştirilebilmesi mümkün olur.

Slotlar, bir bileşenin içinde belirlenmiş bir veya birden fazla alandır ve bu alanlar dış dünyadan içeriğin eklenmesine izin verir. Bir bileşenin içindeki slotlar, bileşenin dışındaki içeriği almak için kullanılabilir.

```html
<my-custom-element>
  <p slot="content">Bu içerik bir slot içine yerleştirilmiştir.</p>
</my-custom-element>
```

Bu örnekte, **`my-custom-element`** adında özelleştirilmiş bir bileşen oluşturulmuştur. Bu bileşenin içinde, **`slot`** adında bir alan tanımlanmıştır. Dış dünyadan içeriğin bu alan içine yerleştirilmesi için **`slot`** adı ile belirtilmiştir. Böylece, bileşenin kullanıldığı yerde, dışarıdan farklı içerikler bu alana yerleştirilebilir ve bileşenin içeriği değiştirilebilir veya özelleştirilebilir.

Slotlar, web bileşenlerinin yeniden kullanılabilirliğini ve esnekliğini artırırken, aynı zamanda bileşenler arasındaki iletişimi ve veri geçişini de kolaylaştırır. Bu sayede, web geliştiriciler, daha modüler ve ölçeklenebilir uygulamalar oluşturabilirler.

## spellcheck

**`spellcheck`**

Numaralandırılmış bir öznitelik, öğenin yazım hatalarına karşı denetlenip denetlenemeyeceğini tanımlar. Aşağıdaki değerlere sahip olabilir:
• `true`öğenin mümkünse yazım hataları açısından kontrol edilmesi gerektiğini belirten boş dize veya ;
• `false`Bu, öğenin yazım hataları açısından kontrol edilmemesi gerektiğini belirtir.

## tabindex

**`tabindex`**, HTML içinde kullanılan bir özelliktir ve bir elementin klavye gezintisi sırasındaki sırasını belirler. Bu özellik, web sayfalarındaki erişilebilirlik (accessibility) ve klavye kullanımını kolaylaştırmak için kullanılır.

Klavye gezintisi sırasında, kullanıcılar genellikle "Tab" tuşunu kullanarak bir web sayfasında gezinirler. **`tabindex`** özelliği, bir elementin bu klavye gezintisi sırasındaki sırasını belirler. Bir elementin **`tabindex`** değeri, o elementin gezinti sırasındaki konumunu belirler. Pozitif bir **`tabindex`** değeri olan elementler, gezinti sırasında öncelikli olarak vurgulanırken, negatif bir **`tabindex`** değeri olan elementler, gezinti sırasında atlanır.

```html
<input type="text" tabindex="1" />
<input type="button" value="Click" tabindex="2" />
<input type="checkbox" tabindex="3" />
```

Bu örnekte, üç farklı form elemanı (**`<input/>`**) bulunmaktadır. Her biri için **`tabindex`** özelliği atanmıştır. **`tabindex`** değerleri küçükten büyüğe doğru sıralanmıştır. Bu, gezinti sırasında öncelikle metin giriş alanına (**`<input type="text"/>`**), ardından butona (**`<input type="button"/>`**) ve son olarak da onay kutusuna (**`<input type="checkbox"/>`**) odaklanılacağını belirtir.

**`tabindex`** özelliği, klavye erişimini kolaylaştırır ve web sayfalarının erişilebilirliğini artırır. Kullanıcıların klavye ile gezinmelerini veya işlemlerini gerçekleştirmelerini daha etkili bir şekilde sağlar. Ancak, **`tabindex`** özelliğini dikkatlice kullanmak önemlidir, çünkü yanlış sıralama veya atanan değerler kullanıcı deneyimini olumsuz etkileyebilir.

## translate

**`translate`**

Bir öğenin öznitelik değerlerinin ve düğüm `[Text](https://developer.mozilla.org/en-US/docs/Web/API/Text)`alt öğelerinin değerlerinin, sayfa yerelleştirildiğinde çevrileceğini veya değiştirilmeden bırakılıp bırakılmayacağını belirtmek için kullanılan numaralandırılmış bir öznitelik. Aşağıdaki değerlere sahip olabilir:
• boş dize veya `yes`; bu, öğenin çevrileceğini belirtir.
• `no`Bu, öğenin çevrilmeyeceğini gösterir.

## virtualkeyboardpolicy

**`virtualkeyboardpolicy`**, HTML içinde kullanılan bir özellik değildir. Ancak, bu terim, genellikle mobil cihazlarda web tarayıcıları ve uygulamalar tarafından kullanılan bir kavramdır.

Mobil cihazlarda, sanal klavyenin (virtual keyboard) kullanımını kontrol etmek ve yönetmek için çeşitli politikalar ve ayarlar bulunur. Bu politikalar, genellikle tarayıcı veya uygulama geliştiricilerinin belirli gereksinimleri veya kullanıcı deneyimini iyileştirmek için belirlenir.

"Virtual keyboard policy" olarak adlandırılan bu politikalar, genellikle şunları içerebilir:

1. Otomatik Klavye Açma: Bir metin giriş alanına tıkladığında veya odaklandığında sanal klavyenin otomatik olarak açılması veya açılmaması.
2. Klavye Görünürlüğü: Sanal klavyenin sayfa üzerinde ne kadar yer kaplayacağını veya ne kadar süre gösterileceğini belirleme.
3. Klavye Tipi: Sanal klavyenin açıldığında varsayılan olarak hangi klavye türünün (örneğin, metin girişi, sayısal, tarih vb.) görüntüleneceğini belirleme.
4. Klavye Kapatma: Kullanıcı bir metin giriş alanından başka bir yere dokunduğunda veya bir form gönderildiğinde klavyenin otomatik olarak kapatılıp kapatılmayacağını belirleme.

Bu politikalar, mobil cihazlarda web tarayıcıları veya uygulamalar aracılığıyla web sayfalarının ve uygulamaların kullanıcı deneyimini daha iyi hale getirmek için önemlidir.
