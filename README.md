# Blue Lock League

GitHub Pages + Supabase tabanlı Blue Lock RP lig istatistik sistemi.

## 1) GitHub
Bu klasörü bir GitHub repository'sine yükle.

## 2) Supabase
Bir Supabase projesi oluştur.
- SQL Editor -> `sql/schema.sql` dosyasını çalıştır.
- Authentication -> Users bölümünden admin hesabı oluştur.
- Oluşan kullanıcının UUID'sini SQL dosyasındaki örnekte `public.profiles` tablosuna admin olarak ekle.

## 3) Frontend bağlantısı
`js/config.js` içindeki:
- SUPABASE_URL
- SUPABASE_ANON_KEY

değerlerini Supabase Project Settings -> API kısmından doldur.

## 4) GitHub Pages
Repository -> Settings -> Pages -> Deploy from branch -> `main` / root.
Site yayınlandıktan sonra `/login.html` admin girişidir.

## Değer sistemi
Gol = 700.000 ₺
Asist = 600.000 ₺
Match Up = 100.000 ₺
Kritik Müdahale = 500.000 ₺

Oyuncu değeri frontend'de bu olayların toplamından hesaplanır. Veritabanı istatistikleri `match_events` kayıtlarından türetilir.

## Admin paneli
Şu anda admin panelinde:
- takım ekleme
- oyuncu ekleme
- maç oluşturma
- maç skoru/status/tarih girme
- maç olayına gol ekleme
- asist ekleme
- Match Up ekleme
- kritik müdahale ekleme
- maç olayını silme
- oyuncuların güncel istatistik ve değerlerini görme

özellikleri çalışır.

İstatistikler `match_events` kayıtlarından otomatik türetilir.

## Önemli not
`js/config.js` içindeki Supabase URL ve ANON KEY girilmeden sadece demo görünümü çalışır. Gerçek admin işlemleri için Supabase bağlantısı şarttır.
