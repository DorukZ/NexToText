# NTT (NexToTask) — Proje Çalışma Rehberi

## Değişmezler
- Ben demeden hiçbir özelliği **silme** / görsel dili kökten **değiştirme**.
- Header/bar: yazılar köşelere yakın; **NTT** butonu **menüyü aç/kapatır**; menü barın üstüne **binmez** (z-index/position). “NexToTask” başlığı **yeşil**.
- Sağ “Görünüm” paneli aynı butonla toggle; **varsayılan filtre = Tümü**.
- Ana ekrandaki **mini takvim** eski görünümüyle kalır.

## Takvim (Google Calendar benzeri)
- Ay görünümünde **gün hücresine çift tık ⇒ Gün görünümü** (timegrid) tam ekran; üstte **Geri** ile Ay’a dön.
- **15 dk slot**, sürükle-bırak & yeniden boyutlandırma; **scroll sadece takvim** konteynerinde.
- Etkinliğe **tek tık ⇒ popover** (başlık, saat, atanmış ekip/kişiler, Tamamla/Sil/Düzenle kısayolu).
- **Çift tık ⇒ düzenleme modali**.
- Tarihler yerel TZ; “bugün” hesabında ofset hatası yok.

## Görevler
- Liste & **Kanban** çalışır; tamamlananlar **ana ekranda gizlenir**, “Görevler” sekmesinde görünür.
- “Yeni Görev” modal akışına dokunma; **Ekip/Kişi ekleme paneli** “Ekle” metniyle açılır.
- Saat seçimleri **15’er dakika** (00/15/30/45).

## Tekrar (zincir)
- Günlük/Haftalık/Aylık **sonsuz** tekrar. Listede yalnız **bugünün örneği** göster.
- Düzenle/saat değiştir/sil sırasında **diyalog**: “Sadece bugün” / “Tüm zincir”.
- Tek occurrence silinince seri **bozulmaz** (exceptions/overrides mantığı).

## Odak
- Başlat/Duraklat/Sıfırla; görev **tamamlanırsa odak biter**.
- Karanlık mod uyumlu mini panel.

## Kapsam
- **Dokunma**: Header/Sidebar yerleşimi, z-index, “Yeni Görev” iş akışı (sadece bug-fix).
- **Düzenlenebilir**: Takvim bileşeni, tekrar motoru, ekip paneli, popover.

## Test / Kabul
1) Ay→Gün çift tık & Geri  
2) 15 dk slot, drag/resize hizası  
3) Scroll sadece takvimde  
4) Tek tık popover, çift tık edit  
5) Görünüm paneli toggle, default **Tümü**  
6) Tekrar düzenlemede diyalog (“bugün vs zincir”), listede yalnız bugünün örneği  
7) Tamamlanan görev → odak biter, ana ekranda gizlenir  
8) Kanban açılıyor/sürükleniyor  
9) Tarih ofseti yok  
10) NTT butonu menüyü aç/kapatır; menü barı kaplamaz
