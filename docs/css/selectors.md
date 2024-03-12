# Selectors

1. **Universal Seçici (\*)**:

- Tüm HTML öğelerini seçmek için kullanılır.

2. **Eleman Seçici (Element Selector)**:

- Belirli bir HTML öğesini seçmek için kullanılır. Örneğin, **`p`** tüm paragrafları seçer.

3. **Sınıf Seçici (Class Selector)**:

- Belirli bir sınıfa ait olan öğeleri seçmek için kullanılır. Örneğin, **`.menu`** HTML'de classı "menu" olan tüm öğeleri seçer.
- Yalnızca belirli bir HTML öğesinin etkilenmesi gerektiğini belirtmek istiyorsanız, sınıf seçiciyle öğe adını kullanmalısınız. Örneğin, **`p.menu`**

4. **ID Seçici (ID Selector)**:

- Belirli bir ID'ye sahip olan öğeyi seçmek için kullanılır. Örneğin, **`#header`** ID'si "header" olan öğeyi seçer.

5. **Grup Seçici (Group Selector)**:

- Birden fazla seçiciyi bir araya getirerek aynı stil kurallarını uygulamak için kullanılır. Örneğin, **`h1, h2, h3`** tüm başlık öğelerini seçer.

6. **Ebeveyn Seçicisi (Parent Selector)**:

- Bir öğenin ebeveynini seçmek için kullanılır. Ancak CSS'de standart bir ebeveyn seçici bulunmamaktadır.

7. **Çocuk Seçicisi (Child Selector)**:

- Bir öğenin belirli bir alt öğesini seçmek için kullanılır. Örneğin, **`ul > li`** bir **`<ul>`** öğesinin doğrudan altındaki **`<li>`** öğelerini seçer.
- Ayrıca **:nth-child()** sıralı çocuk seçicisi kullanılabilir.

```bash
:nth-child(2) ebeveyni içindeki ikinci öğeyi seçer.
:nth-child(odd) ebeveyni içindeki tek sıradaki öğeleri seçer.
:nth-child(3n) ebeveyni içindeki her üçüncü öğeyi seçer.
```

8. **Kardeş Seçicisi (Adjacent Sibling Selector)**:

- Belirli bir öğenin hemen sonraki kardeşini seçmek için kullanılır. Örneğin, **`h2 + p`** bir **`<h2>`** öğesinden sonra gelen ilk **`<p>`** öğesini seçer.

9. **Genel Kardeş Seçicisi (General Sibling Selector)**:

- Belirli bir öğenin sonraki tüm kardeşlerini seçmek için kullanılır. Örneğin, **`h2 ~ p`** bir **`<h2>`** öğesinden sonra gelen tüm **`<p>`** öğelerini seçer.
