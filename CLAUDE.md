# CLAUDE.md

Bu dosya, bu proje üzerinde çalışırken Claude'un (Claude Code dahil) izlemesi gereken bağlamı ve kuralları içerir.

## Proje

**nakliye_yonetim_17v** — _README'de açıklama bulunamadı. Projenin amacını buraya bir-iki cümleyle yazın._

- GitHub: https://github.com/SHapeloglu/nakliye_yonetim_17v

## Teknoloji Yığını

- Odoo 1 modülü (Python + XML view)

## Önemli Dosyalar

- `__manifest__.py`

Mimari ayrıntılar için bkz. `architect.md`.

## Sık Kullanılan Komutlar

```bash
odoo -c <odoo.conf> -u <modul_adi> -d <veritabani>   # modülü güncelle
```

## Kurallar

- Model değişikliğinden sonra modül mutlaka `-u <modul>` ile güncellenmeli; yeni alanlar için view XML ve erişim kuralları (`security/ir.model.access.csv`) birlikte güncellenmeli.
- `__manifest__.py` içindeki `data` listesine eklenmeyen XML dosyaları yüklenmez.
- Odoo çekirdeğini değiştirme; davranışı `_inherit` ile genişlet.
- `.env`, parola, token ve API anahtarlarını asla commit etme.
- Her çalışma oturumunun sonunda `session.md`ye kısa kayıt düş; görev durumunu `task.md`de güncelle.
- Önceliklendirilmemiş fikirleri `backlog.md`ye yaz; somutlaşınca `task.md`ye taşı.

## Çalışma Dosyaları

| Dosya | Amaç |
|---|---|
| `architect.md` | Mimari ve dizin yapısı referansı |
| `task.md` | Aktif / devam eden / tamamlanan görevler |
| `backlog.md` | Önceliklendirilmemiş fikir ve teknik borç havuzu |
| `session.md` | Oturum günlüğü — her oturum sonunda güncellenir |
