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
