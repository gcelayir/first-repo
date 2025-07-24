# Git ve GitHub Rehberi

## İlk Kurulum ve Repository Oluşturma

### 1. Yerel Proje Oluşturma

```cmd
mkdir proje-adi
cd proje-adi
```

**Ne yapar:** Yeni bir klasör oluşturur ve içine girer.

### 2. Git Repository Başlatma

```cmd
git init
```

**Ne yapar:** Bu klasörü Git ile takip edilebilir hale getirir. `.git` klasörü oluşturur.

### 3. Dosyaları Staging Area'ya Ekleme

```cmd
git add .                    # Tüm dosyaları ekler
git add dosya-adi.txt       # Sadece belirtilen dosyayı ekler
```

**Ne yapar:** Dosyaları "staging area"ya ekler, yani commit'e hazırlar.

### 4. Commit Yapma

```cmd
git commit -m "Commit mesajı"
```

**Ne yapar:** Staging area'daki dosyaları kalıcı olarak Git geçmişine kaydeder.

## GitHub ile Bağlantı

### 5. GitHub Repository'sine Bağlanma

```cmd
git remote add origin https://github.com/kullanici-adi/repo-adi.git
```

**Ne yapar:** Yerel repository'yi GitHub'daki repository ile bağlar.

### 6. GitHub'a Yükleme

```cmd
git push -u origin main     # İlk yükleme için
git push                    # Sonraki yüklemeler için
```

**Ne yapar:** Yerel commit'leri GitHub'a yükler.

## Günlük Kullanım Komutları

### Durum Kontrolü

```cmd
git status
```

**Ne yapar:** Hangi dosyaların değiştiğini, hangilerinin staged olduğunu gösterir.

### Değişiklikleri Görme

```cmd
git diff                    # Staged olmayan değişiklikler
git diff --staged          # Staged değişiklikler
```

**Ne yapar:** Dosyalardaki değişiklikleri satır satır gösterir.

### Commit Geçmişi

```cmd
git log                     # Detaylı geçmiş
git log --oneline          # Kısa geçmiş
```

**Ne yapar:** Yapılan commit'lerin geçmişini gösterir.

### GitHub'dan Güncelleme Alma

```cmd
git pull
```

**Ne yapar:** GitHub'daki son değişiklikleri yerel repository'ye indirir.

## Dal (Branch) İşlemleri

### Yeni Dal Oluşturma

```cmd
git branch yeni-dal-adi
git checkout yeni-dal-adi
# veya tek komutla:
git checkout -b yeni-dal-adi
```

**Ne yapar:** Yeni bir dal oluşturur ve o dala geçer.

### Dal Değiştirme

```cmd
git checkout dal-adi
```

**Ne yapar:** Belirtilen dala geçer.

### Dalları Listeleme

```cmd
git branch                  # Yerel dallar
git branch -r              # Uzak dallar
git branch -a              # Tüm dallar
```

### Dal Birleştirme

```cmd
git checkout main
git merge dal-adi
```

**Ne yapar:** Belirtilen dalı ana dala birleştirir.

## Geri Alma İşlemleri

### Son Commit'i Geri Alma

```cmd
git reset --soft HEAD~1     # Commit'i geri al, değişiklikleri koru
git reset --hard HEAD~1     # Commit'i ve değişiklikleri tamamen sil
```

### Dosya Değişikliklerini Geri Alma

```cmd
git checkout -- dosya-adi.txt
```

**Ne yapar:** Dosyadaki değişiklikleri son commit'teki haline döndürür.

### Staging'den Çıkarma

```cmd
git reset dosya-adi.txt
```

**Ne yapar:** Dosyayı staging area'dan çıkarır.

## Kiro'da Git Kullanımı

### Kiro Chat Komutları

- `#Git Diff` - Değişiklikleri gösterir
- `#Terminal` - Terminal'e erişim
- `#Problems` - Kod hatalarını gösterir

### Kiro Panelleri

- **Source Control (Ctrl+Shift+G):** Git işlemleri için
- **Terminal:** Git komutları çalıştırmak için
- **Explorer:** Dosya değişikliklerini görmek için

## Yararlı Git Konfigürasyonu

### Kullanıcı Bilgileri Ayarlama

```cmd
git config --global user.name "Adın Soyadın"
git config --global user.email "email@example.com"
```

### Varsayılan Dal Adını Ayarlama

```cmd
git config --global init.defaultBranch main
```

## Sık Kullanılan İş Akışı

1. **Değişiklik yap** (dosyaları düzenle)
2. **Kontrol et:** `git status`
3. **Değişiklikleri gör:** `git diff`
4. **Ekle:** `git add .`
5. **Commit et:** `git commit -m "Açıklayıcı mesaj"`
6. **Yükle:** `git push`

## GitHub'da Repository Oluşturma Adımları

1. GitHub.com'a git
2. Sağ üst köşedeki "+" → "New repository"
3. Repository adını gir
4. Public/Private seç
5. "Add README" işaretini kaldır (eğer zaten README'n varsa)
6. "Create repository"
7. Verilen komutları terminalde çalıştır

## İpuçları

- **Commit mesajları açıklayıcı olsun:** "Bug fix" yerine "Login sayfasındaki şifre doğrulama hatası düzeltildi"
- **Sık commit yap:** Küçük değişiklikler için bile commit yap
- **Push etmeden önce test et:** Çalışmayan kodu GitHub'a yükleme
- **README.md dosyası ekle:** Projenin ne yaptığını açıkla
- **.gitignore dosyası kullan:** Gereksiz dosyaları Git'ten hariç tut

## Acil Durum Komutları

### Yanlış Commit Mesajını Düzeltme

```cmd
git commit --amend -m "Doğru mesaj"
```

### Son Commit'e Dosya Ekleme

```cmd
git add unutulan-dosya.txt
git commit --amend --no-edit
```

### Tüm Değişiklikleri Silme

```cmd
git reset --hard HEAD
```

Bu rehberi yer imlerine ekle ve ihtiyacın olduğunda kullan!# Git ve GitHub Rehberi

## İlk Kurulum ve Repository Oluşturma

### 1. Yerel Proje Oluşturma

```cmd
mkdir proje-adi
cd proje-adi
```

**Ne yapar:** Yeni bir klasör oluşturur ve içine girer.

### 2. Git Repository Başlatma

```cmd
git init
```

**Ne yapar:** Bu klasörü Git ile takip edilebilir hale getirir. `.git` klasörü oluşturur.

### 3. Dosyaları Staging Area'ya Ekleme

```cmd
git add .                    # Tüm dosyaları ekler
git add dosya-adi.txt       # Sadece belirtilen dosyayı ekler
```

**Ne yapar:** Dosyaları "staging area"ya ekler, yani commit'e hazırlar.

### 4. Commit Yapma

```cmd
git commit -m "Commit mesajı"
```

**Ne yapar:** Staging area'daki dosyaları kalıcı olarak Git geçmişine kaydeder.

## GitHub ile Bağlantı

### 5. GitHub Repository'sine Bağlanma

```cmd
git remote add origin https://github.com/kullanici-adi/repo-adi.git
```

**Ne yapar:** Yerel repository'yi GitHub'daki repository ile bağlar.

### 6. GitHub'a Yükleme

```cmd
git push -u origin main     # İlk yükleme için
git push                    # Sonraki yüklemeler için
```

**Ne yapar:** Yerel commit'leri GitHub'a yükler.

## Günlük Kullanım Komutları

### Durum Kontrolü

```cmd
git status
```

**Ne yapar:** Hangi dosyaların değiştiğini, hangilerinin staged olduğunu gösterir.

### Değişiklikleri Görme

```cmd
git diff                    # Staged olmayan değişiklikler
git diff --staged          # Staged değişiklikler
```

**Ne yapar:** Dosyalardaki değişiklikleri satır satır gösterir.

### Commit Geçmişi

```cmd
git log                     # Detaylı geçmiş
git log --oneline          # Kısa geçmiş
```

**Ne yapar:** Yapılan commit'lerin geçmişini gösterir.

### GitHub'dan Güncelleme Alma

```cmd
git pull
```

**Ne yapar:** GitHub'daki son değişiklikleri yerel repository'ye indirir.

## Dal (Branch) İşlemleri

### Yeni Dal Oluşturma

```cmd
git branch yeni-dal-adi
git checkout yeni-dal-adi
# veya tek komutla:
git checkout -b yeni-dal-adi
```

**Ne yapar:** Yeni bir dal oluşturur ve o dala geçer.

### Dal Değiştirme

```cmd
git checkout dal-adi
```

**Ne yapar:** Belirtilen dala geçer.

### Dalları Listeleme

```cmd
git branch                  # Yerel dallar
git branch -r              # Uzak dallar
git branch -a              # Tüm dallar
```

### Dal Birleştirme

```cmd
git checkout main
git merge dal-adi
```

**Ne yapar:** Belirtilen dalı ana dala birleştirir.

## Geri Alma İşlemleri

### Son Commit'i Geri Alma

```cmd
git reset --soft HEAD~1     # Commit'i geri al, değişiklikleri koru
git reset --hard HEAD~1     # Commit'i ve değişiklikleri tamamen sil
```

### Dosya Değişikliklerini Geri Alma

```cmd
git checkout -- dosya-adi.txt
```

**Ne yapar:** Dosyadaki değişiklikleri son commit'teki haline döndürür.

### Staging'den Çıkarma

```cmd
git reset dosya-adi.txt
```

**Ne yapar:** Dosyayı staging area'dan çıkarır.

## Kiro'da Git Kullanımı

### Kiro Chat Komutları

- `#Git Diff` - Değişiklikleri gösterir
- `#Terminal` - Terminal'e erişim
- `#Problems` - Kod hatalarını gösterir

### Kiro Panelleri

- **Source Control (Ctrl+Shift+G):** Git işlemleri için
- **Terminal:** Git komutları çalıştırmak için
- **Explorer:** Dosya değişikliklerini görmek için

## Yararlı Git Konfigürasyonu

### Kullanıcı Bilgileri Ayarlama

```cmd
git config --global user.name "Adın Soyadın"
git config --global user.email "email@example.com"
```

### Varsayılan Dal Adını Ayarlama

```cmd
git config --global init.defaultBranch main
```

## Sık Kullanılan İş Akışı

1. **Değişiklik yap** (dosyaları düzenle)
2. **Kontrol et:** `git status`
3. **Değişiklikleri gör:** `git diff`
4. **Ekle:** `git add .`
5. **Commit et:** `git commit -m "Açıklayıcı mesaj"`
6. **Yükle:** `git push`

## GitHub'da Repository Oluşturma Adımları

1. GitHub.com'a git
2. Sağ üst köşedeki "+" → "New repository"
3. Repository adını gir
4. Public/Private seç
5. "Add README" işaretini kaldır (eğer zaten README'n varsa)
6. "Create repository"
7. Verilen komutları terminalde çalıştır

## İpuçları

- **Commit mesajları açıklayıcı olsun:** "Bug fix" yerine "Login sayfasındaki şifre doğrulama hatası düzeltildi"
- **Sık commit yap:** Küçük değişiklikler için bile commit yap
- **Push etmeden önce test et:** Çalışmayan kodu GitHub'a yükleme
- **README.md dosyası ekle:** Projenin ne yaptığını açıkla
- **.gitignore dosyası kullan:** Gereksiz dosyaları Git'ten hariç tut

## Acil Durum Komutları

### Yanlış Commit Mesajını Düzeltme

```cmd
git commit --amend -m "Doğru mesaj"
```

### Son Commit'e Dosya Ekleme

```cmd
git add unutulan-dosya.txt
git commit --amend --no-edit
```

### Tüm Değişiklikleri Silme

```cmd
git reset --hard HEAD
```

Bu rehberi yer imlerine ekle ve ihtiyacın olduğunda kullan!
