# NexToText — Final Prototype

NexToText, günlük görevleri takvim üzerinden takip etmek için hazırlanmış responsive web uygulamasıdır.

## Öne çıkanlar
- Profesyonel, responsive masaüstü + mobil arayüz
- Pazartesi başlangıçlı aylık takvim (ayarlar üzerinden Pazar da seçilebilir)
- Sadece **bugün** düzenlenebilir; diğer tarihler salt okunur
- Görev durumları: Tamamlandı / Süreçte / Tamamlanmadı
- Gün detay drawer'ı, hızlı görev ekleme ve görev silme
- Bugün görünümü ve temel performans raporları
- Açık / koyu / sistem teması
- JSON yedekleme ve içe aktarma
- Görev şablonu
- Klavye kısayolu: `Ctrl/Cmd + K` → bugün görev paneli
- Veriler LocalStorage üzerinde kalıcı tutulur
- Harici kütüphane veya build sistemi gerektirmez

## Çalıştırma
Dosyayı doğrudan `index.html` ile açabilirsin. En sağlıklısı küçük bir statik sunucu kullanmaktır:

```bash
python -m http.server 8080
```

Sonra `http://localhost:8080` adresini aç.

## Veri ve güvenlik
Bu sürüm frontend-only bir prototiptir. Veriler cihazın tarayıcısında tutulur. Gerçek çok kullanıcılı/üretim sürümünde server-side kimlik doğrulama, veritabanı, yetkilendirme ve sunucu tarafı yedekleme eklenmelidir.
