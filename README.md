
# Github101 Türkçe Dökümantasyon

## Git ve GitHub, yazılım geliştirme süreçlerinde versiyon kontrolü ve işbirliği yapma olanağı sunan popüler araçlardır. Bu dökümantasyonda, Git ve GitHub'ın temel özellikleri ve kullanımı hakkında bilgiler bulacaksınız.

### İçindekiler

- Git Nedir?
- Git’e Neden İhtiyaç Duyarız?
- Git’in Çalışma Mantığı
- Git’in Yapılandırması
- Git Temel Komutlar
- Git Projesi Oluşturma
- Dosyaları Git Deposuna (Repository) Ekleme
- Git Dosyasındaki Değişiklikler
- Git’ten Dosya Silme
- Projedeki Dosyanın İsmini Değiştirme
- Dosya Taşıma
- Dosyadaki Değişiklikleri Geri Alma
- Versiyon Değiştirme
- Git Dallanma (Branch)
- Uzak Repo’dan Local’e Proje Çekme (Clone)
- Uzak Repodan Değişiklikleri Local Repoya Çekmek (Pull komutu)
- GitHub Nedir?
- GitHub Neden Kullanılır?
- GitHub Repository (Depo) Oluşturma
- GitHub’a Proje Gönderme
- GitHub Branch
- GitHub Issues
- Github Issue Closed

## Git Nedir

Bir versiyon kontrol sistemidir. Yapacağınız projelerin kopyalarını alarak projelerinizin eski versiyonlarına kolaylıkla geri dönmenizi sağlayan bir sistemdir.

> Git sistemi, Linux çekirdeğini yazan Linus Torvalds tarafından geliştirilmiştir. Açık kaynak kodlu özgür yazılım ürünüdür.

## Git Kurulumu
Farklı işletim sistemleri için Git kurulum adımları:


- **Windows:** [Git for Windows](https://gitforwindows.org/) üzerinden indirip kurabilirsiniz.
- **MacOS:** `brew install git` komutu ile Homebrew üzerinden kurabilirsiniz.
- **Linux:** Paket yöneticinize bağlı olarak `sudo apt-get install git` veya `sudo yum install git` komutları ile kurabilirsiniz.

## Git Çalışma Mantığı

Git çalışma mantığı olarak diğer versiyon kontrol sistemlerinden biraz farklıdır. Diğer versiyon kontrol sistemleri, commit işleminde dosyaların değişiklik durumuna göre yeni versiyon kopyasında dosyanın durumunu kaydeder. Ancak git’te her versiyon için projenin tamamının durumu kaydedilir. Çalışma alanı olarak üçe ayrılmaktadır. Çalışma dizinimizde (working directory) git projesi başlatarak işe koyuluruz. Bu alan sistemin ilk alanıdır. Daha sonra çalışma dizinimizdeki dosyaları geçiş bölgesine (staging area) ekleriz. Bu alan sistemin ara alanıdır.


## Git Temel Komutlar
Git'in temel komutları ve kullanımları:

- `git init`: Yeni bir Git deposu başlatır.
- `git add`: Değişiklikleri hazırlama alanına ekler.
- `git commit`: Hazırlanan değişiklikleri kaydeder.
- `git status`: Çalışma dizinindeki değişiklikleri gösterir.
- `git log`: Commit geçmişini gösterir.
- `git diff`: Son commit ile çalışma dizini arasındaki farkları gösterir.
- `git branch`: Mevcut dalları listeler.
- `git checkout`: Belirtilen dala geçer veya belirtilen commit'e gider.
- `git merge`: İki dalı birleştirir.
- `git stash`: Değişiklikleri geçici olarak kaydeder.
- `git rebase`: Bir dal üzerindeki değişiklikleri başka bir dal üzerine uygular.
- `git clone`: Bir Git deposunun kopyasını oluşturur.
- `git pull`: Uzak depodan değişiklikleri alır ve mevcut dal ile birleştirir.
- `git push`: Yerel değişiklikleri uzak depoya gönderir.
- `git remote`: Uzak depoları listeler veya yeni bir uzak depo ekler.
- `git fetch`: Uzak depodan değişiklikleri alır fakat otomatik olarak birleştirmez.
- `git reset`: Belirtilen commit'e kadar olan değişiklikleri geri alır.
- `git rm`: Dosyayı çalışma dizininden ve hazırlama alanından siler.
- `git mv`: Dosyanın adını değiştirir veya taşır.
- `git tag`: Versiyon etiketleri oluşturur veya mevcut etiketleri listeler.
- `git show`: Belirtilen commit, etiket veya dal hakkında bilgi gösterir.
- `git config`: Git ayarlarını yapılandırır.




## Git Yapılandırması

1. Kullanıcı Adı Belirleme.

```sh
git config --global user.name “username”
```

2. E-mail Belirleme

```sh
git config --global user.email “email_adress”
```

## Git Projesi Oluşturma

Proje klasörünün bulunduğu konuma giderek projeyi `git init` komutuyla oluşturabilirsiniz.

## Dosyaları Git Deposuna (Repository) Ekleme

Repository Git projenizin Git tarafından saklandığı yerdir.

```sh
git add .
git commit -m "first commit"
```

Projenizin bir versiyon kopyasını oluşturmuş oldunuz. Birinci satırdaki ‘add‘ komutu dosyaları geçiş bölgesine (staging area) yükle anlamına geliyor.  Add komutunun yanındaki nokta çalışma alanındaki tüm dosyaları geçiş bölgesine gönder anlamına gelir eğer siz belli bir dosya göndermek istiyorsanız o dosyanın adını yazabilirsiniz.

Projede en az bir kere yukardaki yöntem ile repoya dosya yüklediyseniz ve bundan sonra dosyalarınızı geçiş bölgesine eklemeden direk repoya atmak istiyorsanız aşağıdaki kod bloğunu kullanabilirsiniz.

```sh
git commit -am "first commit"
```

Log kayıtlarını görüntülemek

```sh
git log
```

### Git Dosyasındaki Değişiklikler

`status` komutu, çalışma dizininin durumunu ve hazırlama alanını görüntüler.  Hangi değişikliklerin hazırlandığını, hangilerinin yapılmadığını ve hangi dosyaların Git tarafından izlenmediğini görmenizi sağlar.

```sh
git status
```

`diff` komutu, çalışma dizinin durumunu ve hazırlanma alanını satır şeklinde görüntülemenizi sağlar. Sadece belirli dosyalardaki değişikliğe bakmak için dosyanın uazntısını eklemelisiniz.

```sh
git diff
```

```sh
git diff dirctory/
```

## Git’ten Dosya Silme

Git projesinden dosya silmek için iki tane yöntem var. Birincisi direkt çalışma dizininden silmek, ikincisi ise komutlar ile silmek.

Birincisini anlatarak başlıyorum. Proje dosyanıza giderek dosyanızı siliyorsunuz. Ve sırasıyla aşağıdaki komutları yazarak silme işlemini gerçekleştirmiş olursunuz.

```sh
git rm  rm_file/
git commit -m "file deleting”
```

## Git Dosya İsmi Değiştirme

```sh
git mv file_first_name last_name
git commit -m “name change”
```

## Git Dosya Taşıma

```sh
git mv filenameToMove destinationFolder
git commit -m “Migration process”
```

## Dosyadaki Değişiklikleri Geri Alma

Dosyada yapılan değişiklikleri geri almak

```sh
git checkout -- changed_filename
```

Dosyaları `git add` ile ekledikten sonraki değişiklikleri geri almak

```sh
git reset HEAD file_name 
git checkout -- file_name
```

## Versiyon Değiştirme

Bu işlem için git log ile versiyonları sıralıyoruz ve gitmek istediğimiz versiyonun hash kodunu alıyoruz. (Hash code, commit yazısının yanında bulunan kod satırıdır.)

```sh
git checkout version_hash_code -- .
git commit – m “old version copied”
```

## Git Branch

Git projesi oluşturduğunuzda varsayılan olarak main branch oluşur ve siz bu dal üzerinden işlemlerinizi gerçekleştirirsiniz. Bireysel çalışılan bir projede bu yöntem ile bir sıkıntı yaşamazsınız. Ancak çoklu projelerde çalışıyorsanız ve takım üyeleri projenin farklı alanları ile ilgileniyorsa o zaman sıkıntı yaşamaya başlayabilirsiniz. Branch sayesinde her takım üyesi kendi branch‘ında çalışarak diğer takım arkadaşlarının kodlarında değişikliğe sebebiyet vermez. Proje bitiminde merge işlemi ile tüm proje branch’ları main branch’ında birleştirilebilir.

- Branch Listesini Görme

```sh
git branch
```

Not: Aktif olan branch * sembolü ile gösterilir

- Yeni Branch Oluşturma

```sh
git branch new_branch_name
```

- Oluşturulan Branch’a Geçiş Yapmak

```sh
git checkout new_branch_name
```

**Hem branch oluşturup hem de branch’a geçiş yapmak istiyorsanız aşağıdaki kodu kullanabilirsiniz.**

```sh
git checkout -b new_branch_name
```

- Branch’ın İsmini Değiştirmek

```sh
git branch -m new_branch_name newBranch
```

- Branch Silmek

```sh
git branch -D newBranch
```

- Branch’ları Birleştirmek (Merge)

```sh
git merge master newBranch
```

## Uzak Git Sunucusundan HTTP proje çekmek

```sh
git clone https://github.com/username/your_git_repo
```

Örneğin:

```sh
git clone https://github.com/kadirbelkuyu/try.git
```

## Değişiklikleri local sunucunuza çekmek

```sh
git pull
git pull 'remote_address' 'branch_name'
```

# Github Proje Gönderme

```sh
git init
git add .
git commit -m “first commit”
git remote add origin repository_name.git
git push -u origin main
```


## Git İleri Seviye Komutlar ve Kavramlar

### Git Cherry-Pick
Belirli bir commit'i başka bir dal üzerine uygulamak için kullanılır.
```bash
git cherry-pick COMMIT_HASH
```

### Git Bisect
Bir hatanın ne zaman meydana geldiğini bulmak için kullanılır. Git, otomatik olarak commit'leri test ederek hatanın ilk meydana geldiği commit'i bulmanıza yardımcı olur.

### Git Revert
Bir commit'in değişikliklerini geri almak için kullanılır, fakat commit geçmişini değiştirmez.
```bash
git revert COMMIT_HASH
```

## GitHub İleri Seviye Özellikler

### GitHub Actions ile CI/CD
GitHub Actions, kodunuzu otomatik olarak test etmek ve dağıtmak için kullanabileceğiniz bir CI/CD aracıdır. `.github/workflows` klasörü altında YAML formatında iş akışı tanımlamaları yapabilirsiniz.

### GitHub Code Review
Pull request'ler üzerinde kod incelemesi yapma, yorum bırakma ve değişiklik önerme.

### GitHub Packages
Kütüphanelerinizi ve uygulamalarınızı GitHub üzerinde depolama ve dağıtma olanağı.

## Git ve GitHub İle İlgili İpuçları

1. **Atomik Commit'ler:** Her commit'in tek bir değişikliği yansıtmasına özen gösterin. Bu, gelecekte değişiklikleri takip etmeyi ve hataları bulmayı kolaylaştırır.
2. **Açıklayıcı Commit Mesajları:** Commit mesajlarınızın, değişikliğin neden yapıldığını açıkça belirtmesi önemlidir.
3. **Pull Request Kullanımı:** Yeni bir özellik eklerken veya bir hatayı düzeltirken, bu değişiklikleri ana dalınıza doğrudan eklemek yerine bir pull request oluşturun. Bu, kod incelemesi yapmayı ve hataları önceden yakalamayı kolaylaştırır.

## Sıkça Sorulan Sorular

- **Q:** Git'te "detached HEAD" ne demektir?
    - **A:** HEAD, şu anki dalınızın en son commit'ini işaret eder. "Detached HEAD", HEAD'in spesifik bir commit'i işaret ettiği, herhangi bir dalda olmadığı anlamına gelir.

- **Q:** GitHub'da forking ne demektir?
    - **A:** Forking, bir başkasının GitHub deposunun kendi hesabınıza bir kopyasını oluşturmanız anlamına gelir. Bu, projeye katkıda bulunmak için kullanılır.

---


## Gelişmiş Konular

### Git Hooks
Git Hooks, Git komutları çalıştırıldığında otomatik olarak tetiklenen scriptlerdir. Örneğin, bir commit oluşturmadan önce belirli bir testi çalıştırmak isterseniz `pre-commit` hook'unu kullanabilirsiniz.
```bash
# .git/hooks/pre-commit
#!/bin/sh
npm test
```

### Git Submodules
Bir Git deposunda başka bir Git deposunu alt modül olarak kullanabilirsiniz. Bu, bağımlılıkları yönetmek için kullanışlıdır.
```bash
git submodule add [URL] [klasör_adı]
```

### .gitignore
Git'in izlememesi gereken dosyaları veya klasörleri belirtir. Örneğin, `node_modules` klasörünü izlemek istemiyorsanız:
```
# .gitignore dosyası
node_modules/
```

## GitHub Özellikleri

### GitHub Actions
Kodunuzu otomatik olarak test etmek, derlemek ve dağıtmak için kullanabileceğiniz bir CI/CD aracıdır. Örneğin, bir Node.js uygulamasını test etmek için:
```yaml
# .github/workflows/main.yml
name: Node.js CI
on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    - name: Use Node.js
      uses: actions/setup-node@v1
      with:
        node-version: '18.x'
    - run: npm install
    - run: npm test
```

### GitHub Pages
Statik web siteleri barındırma. Örneğin, `docs` klasöründeki HTML dosyalarınızı GitHub Pages ile yayınlamak için repository ayarlarınızda GitHub Pages bölümünden `docs` klasörünü seçin.

### GitHub Gists
Kod parçacıklarını paylaşma. Gists, tek bir dosya veya birden fazla dosya içeren küçük kod parçacıkları için idealdir. Gists, özel veya herkese açık olabilir.

## En İyi Uygulamalar

### Commit Mesajları
Açıklayıcı ve anlamlı commit mesajları yazın. Örneğin:
```
Kötü: Bug fix
İyi: Kullanıcı kaydı sırasında yaşanan hata düzeltildi
```

### Branch Stratejileri
Farklı özellikler veya hata düzeltmeleri için farklı dallar kullanın. Genelde `feature`, `develop`, `master` gibi branch yapıları kullanılır.

## Sıkça Karşılaşılan Sorunlar ve Çözümleri

### Merge Conflicts
İki dal birleştirilirken aynı satırda yapılan değişikliklerden dolayı çakışmalar olabilir. Bu çakışmaları manuel olarak çözmeniz gerekir.

### Detached HEAD
"Detached HEAD" durumu, HEAD'in spesifik bir commit'i işaret ettiği, herhangi bir dalda olmadığı anlamına gelir. Bu durumdan çıkmak için yeni bir dal oluşturabilir veya mevcut bir dala geri dönebilirsiniz.
```bash
git checkout -b yeni_dal_adı
```
veya
```bash
git checkout mevcut_dal_adı
```




