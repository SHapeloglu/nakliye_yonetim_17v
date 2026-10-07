# CLAUDE.md — Nakliye Yönetim (Odoo 17 sürümü)

> 🗄️ **ARŞİV (2026-10-07):** Odoo 17 sürümü artık geliştirilmiyor. Bu repodaki tek kod commit'i (`66bb557`) Odoo 18 reposunun geçmişinde aynen var; güncel modül: **[SHapeloglu/nakliye_yonetim](https://github.com/SHapeloglu/nakliye_yonetim)** (Odoo 18). Odoo 17 gerekirse oradaki 2026-07-20 düzeltmeleri (zorunlu alanlar, partner değişiklikleri) geri taşınmalı.

Şantiye bazlı nakliye operasyonları için özel Odoo modülü: şantiye/saha tanımları, nakliyeci sözleşmeleri, günlük plan, döküm/kantar/yakıt fişleri, yemek planı ve puantajı, taşeron **hakediş** hesaplama + PDF, satır bazlı yetkilendirme (formen / şantiye muhasebecisi).

- GitHub: https://github.com/SHapeloglu/nakliye_yonetim_17v — **Odoo 17 sürümü, 2026-06-25'ten beri güncellenmiyor**
- **Aktif sürüm (Odoo 18):** ayrı public repo `SHapeloglu/nakliye_yonetim`, sunucuda `/opt/odoo/custom_addons/nakliye_yonetim` (prod/test Odoo 18 servisleri yüklüyor). Fark: `tree` → `list` görünümleri, menü `path` alanları, bazı alanların `required=True` olması ve 2026-07-20 güncellemeleri.
- Ayrıntılı spesifikasyon: `nakliye_yonetim_spec.md` · Mimari: `architect.md` · Görevler: `task.md` · Fikirler: `backlog.md` · Günlük: `session.md`

## Kurallar

- **Yeni geliştirme Odoo 18 reposunda yapılır.** Bu repoda değişiklik yalnızca Odoo 17 müşterisi için gerekiyorsa — önce kullanıcıya sor.
- Model / alan / iş kuralı değişikliğinde `nakliye_yonetim_spec.md`'yi güncelle (tek doğruluk kaynağı).
- Odoo 17 sözdizimi: liste görünümü `<tree>`, `attrs`/`states` yerine 17'de `invisible="..."` ifadeleri.
- Yeni model = `security/ir.model.access.csv` satırları + gerekiyorsa `ir_rule.xml` kuralı (formen/muhasebeci izolasyonu).
- `__pycache__/*.pyc` izleniyor (bu repoda `.gitignore` sonradan eklenmiş) — yeni pyc ekleme.
- Oturum sonunda `session.md`'ye kayıt düş, `task.md`'yi güncelle.
