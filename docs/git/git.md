# Git Basics

## GitHub repository oluşturma

1. **Yeni Bir Repository Oluşturma:**
- GitHub hesabınıza giriş yapın.
- Üst menüde bulunan artı (+) işaretine tıklayarak "New repository" seçeneğini seçin.
- Gerekli bilgileri doldurun: repo adı, açıklama, gizlilik seçenekleri vb.
- Oluştur butonuna tıklayarak yeni bir repo oluşturun.

2. **Yerel Projeyi Başlatma ve Ayarlama:**
- Yerel bir dizin oluşturun veya mevcut bir dizine gidin.
- Git'i bu dizinde başlatın:

```bash
git init
```
> Projenizin dosyalarını bu dizine ekleyin.

3. **Değişiklikleri İzleme Alanına Ekleyin (Staging):**
- Yapılan değişiklikleri izleme alanına eklemek için **git add** komutunu kullanın. Örneğin:

```bash
git add .
```
> Burada, . işareti tüm değişiklikleri ekler.

4. **Yapılan Değişiklikleri Commit Etme:**
- Değişiklikleri bir commit'e dönüştürmek için **git commit** komutunu kullanın:

```bash
git commit -m "first commit"
```
> -m , commit mesajını doğrudan komut satırından girmenizi sağlar. Mesaj, yapılan değişiklikleri açıklamalıdır.

5. **Uzak Depoya (remote repository) Bağlanma:**
- GitHub'daki uzak depoya bağlanmak için, projenizi orijinal depo olarak ekleyin:

```bash
git remote add origin [uzak depo urlsi]
```
6. **Değişiklikleri Uzak Depoya(remote repository) İtmek:**
- Local repository’deki değişiklikleri GitHub'daki remote repository’e göndermek için **git push** komutunu kullanın:

```bash
git push -u origin main
```
> -u , local main branch’e remote main branch’i izlemesini söyler.

## Branch oluşturmanın iki yolu var:

- Sadece branch oluşturur ama o branche geçmez.

```bash
git branch [branch ismi]
```

> Örneğin main branchindeyken "git branch development" yaparsam "development" isminde yeni bir branch oluşturur ama mevcut branchim "git checkout development" yapana kadar main olarak kalır.

- Branch oluşturur ve oluşturduğu branche geçer

```bash
git checkout -b [branch ismi]
```

> Örneğin "main" branchindeyken "git checkout -b development" yaparsam "development" isminde bir branch oluşturur ve mevcut branchi "development" olarak değiştirir.

## Branch değiştirmenin tek yolu var:

```bash
git checkout [branch ismi]
```

> Yalnızca bir branchten diğer branche geçmemi sağlar. Örneğin "main" branchindeyken "git checkout development" yaparsam mevcut branchim "development" olur.

## Branchleri listelemenin tek yolu var:

```bash
 git branch
```

> :q ile çıkılır

## Branch nasıl silinir?

```bash
 git branch -d [branch ismi]
```

## Commit historysine nasıl bakılır?

```bash
 git log
```

## Repo nasıl klonlanır? 

```bash
 git clone [reponun linki]
```

## Terminalden bir klasörü silmek için:

```bash
 rm -rf [klasör ismi]
```

```bash
 rm [dosyanın ismi]
```

> Sadece bir dosyayı silmek için

## Repodaki tüm değişiklikleri uzak sunucudan çekmek için:

```bash
 git fetch
```

## Sadece branchtekini çekmek için:

```bash
 git pull [remote sunucu ismi] [branch ismi]
```

> Örnek: git pull origin main

## Başka bir branchi kendi branchinle birleştirmek için:

```bash
 git merge [branch ismi]
```

> Örneğin main branchindeyken "git merge development" yaparsam "development" branchi içindeki değişiklikleri main branchinin içine alır.

## Branchimdeki değişiklikleri github’a yollamak için:

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

- Main branchin pull ya da fetch ile güncel hali alındıktan sonra onun üzerine yeni bir branch açılır.
- Yeni bir branch açarken main branch içindeyken açılması gerekiyor. Başka branch üzerinden açılırsa oradaki değişiklikleri de dahil eder.
- **Değişiklikler yapıldıktan sonra**:  “(git add .) (git commit - m “commit message”)  (git push [sunucu ismi] [branch ismi]) ile github’a değişiklikler bildirilir.
- **Pull Request Açın:** GitHub web arayüzünden, reponuzun ana sayfasında bulunan "Pull Request" veya "New Pull Request" butonuna tıklanır. Karşınıza çıkan sayfada, hangi branch'i hangi branch'e merge etmek istediğiniz seçilir ve açıklama ekleyerek PR oluşturulur.
- **İnceleme ve Onay:** PR'ı oluşturduktan sonra, projenin sahipleri veya diğer katkıda bulunanlar tarafından incelenir ve gerektiğinde değişiklikler istenebilir. Son olarak, PR projenin ana branch'ine merge edilirse, değişiklikler projeye dahil olur.

## Conflict çıkarsa ne yapılması gerekiyor?
 
**Conflict Durumunu Belirleme:**
- Conflict durumları genellikle birleştirme (merge) işlemi sırasında ortaya çıkar. GitHub'da bir PR (Pull Request) birleştirmeye çalıştığınızda veya bir dalı ana dala (main) birleştirmeye çalıştığınızda conflict oluşabilir.

**Conflict'i Çözme:**

- İlk adım, çakışan dosyaları belirlemektir. Genellikle bu, terminal veya Git istemcisi üzerinden yapılır.
- Çakışan dosyaları düzenleyin. Çakışan dosyalar, çakışma işaretleri ile işaretlenmiş olacak ve çakışan değişiklikler arasında size rehberlik edecektir.
- Conflict'i çözün ve dosyaları istediğiniz gibi düzenleyin.
- Dosyaları kaydedin ve çözümlerinizi işleyin.

**Çözümleri Commit Etme:**

- Çakışmayı çözdükten sonra, değişiklikleri commit edin. Bu, yerel çalışma kopyanızda gerçekleşir.
-Commit mesajını açıklayıcı bir şekilde yazın, çünkü bu çözümü projenizin geçmişine kaydedecektir.

**Değişiklikleri Ana Dal Üzerine İtmek (Push):**

- Çözümleri yerel çalışma kopyanızda commit ettikten sonra, değişiklikleri ana dala (main/master) veya ilgili dalınıza itmeniz gerekecektir.
- Bunun için git push komutunu kullanabilirsiniz.

**Pull Request veya Ana Dalı Güncelleme:**

- Eğer bir PR üzerinde conflict çıktıysa, PR'ı güncellemek ve çakışmayı çözmek için PR sayfasında talimatları izleyin.
- Eğer ana dalda (main/master) bir conflict varsa, bu değişiklikleri ana dala ittikten sonra, gerekirse PR'ları güncellemeniz gerekebilir.

**Gerekirse İnceleyin ve Onay Alın:**

- Son olarak, gerekirse projenin diğer katılımcılarıyla iletişime geçin ve çakışmayı çözdüğünüzü onaylamalarını isteyin.


