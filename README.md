[README.md](https://github.com/user-attachments/files/35426913/README.md)
# PC-TOOLS

Windows sistem bakımı, temizliği, donanım analizi, ağ güvenliği ve onarımı için Python (CustomTkinter) ile geliştirilmiş modüler açık kaynaklı masaüstü araç seti.

**SERDAR.B & ATLAS**

## Özellikler

- **Çift Modlu Arayüz (Basit & Uzman):**
  - **Hızlı Bakım (Tek Tık):** Güvenli modülleri tek tuşla tarar, temizler ve sonucu özetler.
  - **Uzman Paneli:** Her modül için ayrıntılı tarama kartları, seçmeli işlem ve teşhis raporu sunar.
- **Tak-Çalıştır Modüler Mimari (`modules/`):**
  - `01_cleaner.py` — **Bilgisayar Temizliği:** Kullanıcı/Windows Temp, hata raporları (WER/CrashDump), Prefetch, Windows Update önbelleği, Chrome/Edge önbelleği ve Geri Dönüşüm Kutusu.
  - `02_repair.py` — **Sistem Taraması ve Onarım:** `SFC`, `DISM` ve `CHKDSK` bütünlük denetimi, onarımı ve onarım sonrası doğrulama.
  - `03_sysinfo.py` — **Sistem Bilgileri:** İşletim sistemi, CPU, RAM, önyükleme kısıtları (`bcdedit`), diskler, GPU, ağ durumu ve çalışma süresi.
  - `04_speedtest.py` — **İnternet Hız Testi:** Ookla `speedtest.exe` CLI ile ping, jitter, indirme ve yükleme ölçümü.
  - `05_net_security.py` — **Ağ Güvenliği Testi:** Dinleyen portlar, etkin TCP oturumları ve Windows Güvenlik Duvarı profil denetimi.
  - `06_net_repair.py` — **Ağ Bağlantısı Onarım Aracı:** DNS önbelleği temizleme, Winsock ve TCP/IP sıfırlama, IP yenileme.
- **Çoklu Dil Desteği (`locales/`):** Türkçe (`tr`), İngilizce (`en`) ve Almanca (`de`) anlık dil geçişi.
- **Tema & Güncelleme Kontrolü:** Koyu / Açık / Sistem teması desteği ve GitHub Releases sürüm denetimi (`core/updater.py`).

## Gereksinimler

- Windows 10 / 11 (64-bit)
- Python 3.10+ (Test edilen: Python 3.12)
- Sistem onarımı ve ağ sıfırlama işlemleri için Yönetici (Administrator) yetkisi

## Kurulum ve Çalıştırma

1. Depoyu bilgisayarınıza indirin:
   ```bash
   git clone https://github.com/selenler/pc-tools.git
   cd pc-tools
   ```
2. Gerekli kütüphaneleri yükleyin:
   ```bash
   pip install -r requirements.txt
   ```
3. Uygulamayı başlatın:
   ```bash
   python main.py
   ```
   *(Windows üzerinde yönetici yetkisiyle doğrudan başlatmak için `BASLAT_GUI.bat` dosyasını da kullanabilirsiniz.)*

## Yeni Modül Geliştirme

Yeni bir bakım aracını veya `.bat` betiğini arayüze eklemek için [docs/MODULE_DEVELOPMENT_GUIDE.md](docs/MODULE_DEVELOPMENT_GUIDE.md) kılavuzunu ve [docs/templates/module_template.py](docs/templates/module_template.py) şablonunu inceleyebilirsiniz.

## Lisans

Bu proje [LICENSE](LICENSE) dosyasında belirtilen şartlar altında açık kaynak olarak sunulmaktadır.
