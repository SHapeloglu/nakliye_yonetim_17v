# Nakliye Yönetim — Odoo 17 Modülü

> 🗄️ **ARŞİV (2026-10-07):** Odoo 17 sürümü artık geliştirilmiyor. Bu repodaki tek kod commit'i (`66bb557`) Odoo 18 reposunun geçmişinde aynen var; güncel modül: **[SHapeloglu/nakliye_yonetim](https://github.com/SHapeloglu/nakliye_yonetim)** (Odoo 18). Odoo 17 gerekirse oradaki 2026-07-20 düzeltmeleri (zorunlu alanlar, partner değişiklikleri) geri taşınmalı.

Şantiye bazlı nakliye operasyonlarını (araç sefer takibi, kantar / döküm / yakıt fişleri, yemek planlaması, taşeron hakediş hesaplama) uçtan uca yöneten özel Odoo modülü.

> ℹ️ Bu repo modülün **Odoo 17** sürümüdür. Aktif geliştirme **Odoo 18** sürümünde yapılmaktadır: [SHapeloglu/nakliye_yonetim](https://github.com/SHapeloglu/nakliye_yonetim).

📄 Ayrıntılı teknik spesifikasyon (modeller, alanlar, iş kuralları, güvenlik, menüler): [`nakliye_yonetim_spec.md`](nakliye_yonetim_spec.md)

## Ne işe yarar?

- Araçların hangi şantiye/sahada, hangi işte (moloz, döküm, mıcır, kum, stabilize) çalışacağının **günlük planlanması**
- Fiili seferlerin kaydı: **döküm fişi** (km), **kantar fişi** (tonaj, araç yük haddi aşımı), **yakıt fişi**
- Şantiye personeli ve taşeron işçileri için **yemek planı ve puantajı**
- Nakliyeci firmalara **sözleşme fiyatlarına göre hakediş** hesaplama, onay akışı ve **PDF rapor**
- Personel zimmet takibi (`maintenance.equipment`)

## Bağımlılıklar

`base`, `mail`, `account`, `hr`, `fleet`, `maintenance`

## Kurulum

1. Klasörü Odoo 17 `addons_path` içindeki bir dizine kopyalayın.
2. Odoo'yu yeniden başlatın, *Uygulamalar* → *Uygulama Listesini Güncelle*.
3. **Nakliye Yönetim** modülünü kurun.

## Yetki grupları

Formen → Yönetici Formen → Şantiye Muhasebecisi → Muhasebe Müdürü → Yönetim → Admin.
Formen yalnız atandığı sahaları, şantiye muhasebecisi yalnız kendi şantiyesini görür (`ir.rule`).

## Zamanlanmış görevler

- Sözleşme bitiş tarihi kontrolü (günlük)
- Onay bekleyen hakediş hatırlatması (günlük)
