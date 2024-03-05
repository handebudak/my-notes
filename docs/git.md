# Git Basics

**Branch oluşturmanın iki yolu var**

- Sadece branch oluşturur ama o branche geçmez.

```bash
git branch [branch_ismi]
```

> Örneğin main branchindeyken "git branch development" yaparsam "development" isminde yeni bir branch oluşturur ama mevcut branchim "git checkout development" yapana kadar main olarak kalır.

- Branch oluşturur ve oluşturduğu branche geçer

```bash
git checkout -b [branch_ismi]
```

> Örneğin "main" branchindeyken "git checkout -b development" yaparsam "development" isminde bir branch oluşturur ve mevcut branchi "development" olarak değiştirir.

**Branch değiştirmenin tek yolu var**

```bash
git checkout [branch_ismi]
```

> Yalnızca bir branchten diğer branche geçmemi sağlar. Örneğin "main" branchindeyken "git checkout development" yaparsam mevcut branchim "development" olur.

**Branchleri listelemenin tek yolu var**

```bash
 git branch
```

> :q ile çıkılır

**Branch nasıl silinir**

```bash
 git branch -d [branch ismi]
```

**Commit historysine nasıl bakılır**

```bash
 git log
```

**Repo nasıl klonlanır**

```bash
 git clone [reponun linki]
```

**Terminalden bir klasörü silmek için**

```bash
 rm -rf [klasör ismi]
```

```bash
 rm [dosyanın ismi]
```

> Sadece bir dosyayı silmek için

**Repodaki tüm değişiklikleri uzak sunucudan çekmek için**

```bash
 git fetch
```

**Sadece branchtekini çekmek için**

```bash
 git pull [remote sunucu ismi] [branch ismi]
```

> Örnek: git pull origin main

**Başka bir branchi kendi branchinle birleştirmek için**

```bash
 git merge [branch ismi]
```

> Örneğin main branchindeyken "git merge development" yaparsam "development" branchi içindeki değişiklikleri main branchinin içine alır.

**Branchimdeki değişiklikleri github’a yollamak için**

```bash
 git push [remote sunucu ismi] [branch ismi]
```

> Örnek: git push origin main 

## PR nasıl açılır, açılmadan önce nelere dikkat edilir?

- PR açmadan önce, asıl branch neyse onun en güncel hali alınır ve kendi branchine merge yapılır.

```bash
git checkout [asıl branch adı]
git pull [remote sunucu ismi (origin)] [branch ismi]
git checkout [diğer branchin adı]
git merge [asıl branch adı]
git push [remote sunucu adı (origin)] [branch ismi]
```

- Main branchi pull ya da fetch ile güncel hali alındıktan sonra onun üzerine yeni bir branch açılır.
- Yeni bir branch açarken main branch içindeyken açmam gerekiyor. Başka branch üzerinden açılırsa oradaki değişiklikleri de dahil eder.
- **Değişiklikler yapıldıktan sonra**:  “(git add .) (git commit - m “commit message”)  (git push [sunucu ismi] [branch ismi]) ile github’a değişiklikler bildirilir.
- **Pull Request Açın:** GitHub web arayüzünden, reponuzun ana sayfasında bulunan "Pull Request" veya "New Pull Request" butonuna tıklanır. Karşınıza çıkan sayfada, hangi branch'ı hangi branch'a merge etmek istediğiniz seçilir ve açıklama ekleyerek PR'ı oluşturulır.
- **İnceleme ve Onay:** PR'ı oluşturduktan sonra, projenin sahipleri veya diğer katkıda bulunanlar tarafından incelenir ve gerektiğinde değişiklikler istenebilir. Son olarak, PR projenin ana branch'ine merge edilirse, değişiklikler projeye dahil olu

## Conflict çıkarsa ne yapılması gerekiyor?

- VScode’da “Source Control” kısmından “Merge Changes” dosyası içindekilere gelip (+) işaretine basılır.
- Daha sonra terminalde “git push [remote sunucu adı (origin)] [branch ismi]” girilirse PR güncellenir.
