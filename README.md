# Bi’ Kutu Oyun · Panel

Projeler, ürün takvimi, fikir atlası, toplantılar, arşiv ve kayıtlar.

## Dosyalar
- `panel.dc.html`: uygulamanın kendisi
- `index.html`: panele yönlendirir
- `support.js`: çalışma dosyası (dokunma)
- `firebase-config.js`: Firebase bilgilerin (bir kez doldurulacak)
- `firestore.rules`: veritabanı güvenlik kuralları
- `assets/`: logo

## Kurulum
1. Firebase Console'da proje oluştur.
2. **Authentication > Sign-in method > Email/Password**'ü aç.
3. **Firestore Database > Create database**'e bas (Production mode).
4. **Firestore > Rules** sekmesine `firestore.rules` içeriğini yapıştırıp **Publish**'e bas.
5. **Proje ayarları > Web uygulaması ekle**'yi seç, çıkan `firebaseConfig` değerlerini `firebase-config.js`'e yapıştır.
6. GitHub Pages'i aç: **Settings > Pages > Deploy from branch > main / root**.
7. **Authentication > Settings > Authorized domains**'e `KULLANICIADI.github.io` alan adını ekle.
8. İlk admin hesabını Firebase Console'dan elle oluştur: **Authentication > Add user** (`kullaniciadi@bikutuoyun.panel`), sonra **Firestore > users** koleksiyonuna o kullanıcının UID'siyle `username`, `name`, `admin: true` alanlarını içeren bir kayıt ekle.
9. Sol alttaki ⚙︎ çarkından ekip üyelerini ekle.

Not: Firebase ayarları doldurulmazsa site "demo modunda" açılır ve veriler yalnızca o tarayıcıda tutulur.
