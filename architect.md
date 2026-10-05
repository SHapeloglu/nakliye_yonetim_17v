# architect.md — nakliye_yonetim_17v Mimari Referansı

Bu dosya projenin yapısının hızlı-referans özetidir. Kod değiştikçe güncel tutun.

## Genel Bakış

_README'de açıklama bulunamadı. Projenin amacını buraya bir-iki cümleyle yazın._

## Teknoloji Yığını

- Odoo 1 modülü (Python + XML view)

## Dizin Yapısı

```
.gitignore
__init__.py
__manifest__.py
data/
models/
  __init__.py
  ayarlar.py
  dokum_fisi.py
  employee_santiye.py
  equipment.py
  gunluk_plan.py
  hakedis.py
  hr_employee.py
  kantar_fisi.py
  partner.py
  saha.py
  santiye.py
  sozlesme.py
  yakit_fisi.py
  yemek_plan.py
  yemek_puantaj.py
nakliye_yonetim_analiz.docx
nakliye_yonetim_spec.md
report/
  __init__.py
  hakedis_report.xml
security/
  groups.xml
  ir.model.access.csv
  ir_rule.xml
views/
  ayarlar_views.xml
  dokum_fisi_views.xml
  equipment_views.xml
  gunluk_plan_views.xml
  hakedis_views.xml
  hakedis_wizard_views.xml
  hr_employee_views.xml
  kantar_fisi_views.xml
  partner_views.xml
  …
```

## Modüller / Kaynak Dosyalar

- `__manifest__.py`
- `models/ayarlar.py`
- `models/dokum_fisi.py`
- `models/employee_santiye.py`
- `models/equipment.py`
- `models/gunluk_plan.py`
- `models/hakedis.py`
- `models/hr_employee.py`
- `models/kantar_fisi.py`
- `models/partner.py`
- `models/saha.py`
- `models/santiye.py`
- `models/sozlesme.py`
- `models/yakit_fisi.py`
- `models/yemek_plan.py`
- `models/yemek_puantaj.py`
- `wizard/hakedis_wizard.py`

## Giriş Noktaları ve Yapılandırma

- `__manifest__.py`

## Dağıtım / Çalışma Ortamı

- GitHub: https://github.com/SHapeloglu/nakliye_yonetim_17v

## Diğer Dokümanlar

- `nakliye_yonetim_spec.md`

## Mimari Kararlar

_Önemli tasarım kararlarını ve gerekçelerini buraya ekleyin (ör. "X yerine Y seçildi çünkü ...")._
