# Lab 1: Switch Fundamentals & L2 Operations (Switch Temelleri ve Katman 2 Operasyonları)

Cisco Packet Tracer üzerinde gerçekleştirdiğim temel ağ yapılandırma ve Katman 2 (L2) davranış analizi çalışması.

---

## 📌 Uygulama Özeti
Bu çalışmada Cisco 2960 Switch üzerinde temel L1/L2 ayarları yapılmış, konsol kablosu üzerinden CLI erişimi sağlanmış ve anahtarın (switch) cihazlara ait MAC adreslerini nasıl öğrendiği doğrulanmıştır.

## 🌐 Topoloji
![Lab 1 Topology](lab1-topology.png)

## 🛠️ Yapılan İşlemler
- `PC-A` RS-232 portundan Switch Console portuna mavi konsol kablosu bağlanarak Terminal üzerinden CLI erişimi sağlandı.
- Switch cihaz adı `SW1` olarak değiştirildi.
- `Fa0/1` ve `Fa0/2` portlarının hızı `100 Mbps`, iletişim modu ise `full duplex` olarak sabitlendi.
- Yapılan konfigürasyon `write` (`wr`) komutu ile NVRAM belleğine kalıcı olarak kaydedildi.
- `PC-A` (`192.168.1.10`) cihazından `PC-B` (`192.168.1.20`) cihazına ping atılarak L2 trafiği başlatıldı.

## 📊 CLI Doğrulaması
Ping işlemi sonrasında `SW1` üzerinde `show mac address-table` komutu çalıştırıldı. `Fa0/1` ve `Fa0/2` portlarının karşısında cihazlara ait MAC adreslerinin dinamik olarak öğrenildiği teyit edildi.

![Lab 1 MAC Table](lab1-mac-table.png)
