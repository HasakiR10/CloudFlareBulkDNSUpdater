![Cloudflare DNS Güncelleyici Logo](https://github.com/HasakiR10/CloudFlareBulkDNSUpdater/blob/main/assets/cksdebk.jpg)
# Cloudflare DNS Güncelleyici

Bu depo, Cloudflare'daki DNS kayıtlarını güncellemek için güçlü ve verimli bir araç içermektedir. Kullanım kolaylığı ve sağlam işlevsellik odaklı olarak tasarlanan bu araç, kullanıcıların DNS A kayıtlarını zahmetsizce güncellemelerini sağlar ve alan adlarının her zaman doğru IP adresine işaret ettiğinden emin olur.

## Özellikler

- **Otomatik DNS Güncellemeleri**: Tüm Cloudflare bölgelerinizdeki A kayıtlarını yeni bir IP adresi ile sorunsuz bir şekilde güncelleyin.
- **Esnek Kayıt Seçimi**: Tüm A kayıtlarını veya yalnızca bölgenin kök adını eşleyen kayıtları güncellemeyi seçin.
- **Güvenli Kimlik Doğrulama**: Cloudflare API tokenlarını kullanarak güvenli bir şekilde kimlik doğrulama ve Cloudflare API'si ile etkileşimde bulunun.

## Başlangıç

### Gereksinimler

- .NET Core SDK
- Cloudflare hesabı ve API jetonu
- İnternet bağlantısı

### Kurulum

1. Depoyu klonlayın:

    ```sh
    git clone https://github.com/HasakiR10/CloudFlareBulkDNSUpdater.git
    cd CloudFlareBulkDNSUpdater
    ```

2. Cloudflare API jetonunuzu, yeni IP adresinizi ve tüm A kayıtlarını mı yoksa sadece kök kayıtları mı güncellemek istediğinizi girmeniz istenecektir.

### Örnek

Uygulamayı çalıştırdıktan sonra, sizden Cloudflare API jetonunuzu, DNS kayıtlarınız için ayarlamak istediğiniz yeni IP adresinizi ve tüm A kayıtlarını mı yoksa sadece kök kayıtları mı güncellemek istediğinizi girmeniz istenecektir. Uygulama daha sonra bölgelerinizi alacak, ilgili A kayıtlarını getirecek ve belirtilen şekilde güncelleyecektir.

### Kod Genel Bakış

Kod, anlaşılabilirlik ve değiştirilebilirlik açısından basit bir şekilde yapılandırılmıştır:

- **Ana Metot (Main Method)**: Kullanıcı girişlerini okumaktan DNS kayıtlarını güncellemeye kadar olan iş akışını düzenler.
- **GetZones Metodu**: Tüm bölgeleri Cloudflare'dan alır.
- **GetARecords Metodu**: Belirli bir bölge için A kayıtlarını getirir.
- **UpdateDnsRecord Metodu**: Belirli bir DNS kaydını yeni IP adresi ile günceller.

### Hata Yönetimi

API istekleri sırasında karşılaşılan sorunların kullanıcıya net bir şekilde iletilmesini sağlamak için kapsamlı bir hata yönetimi uygulanmıştır.

### Katkıda Bulunma

Katkılarınızı bekliyoruz! Lütfen depoyu forkladıktan sonra bir dal oluşturun ve değişikliklerinizle birlikte bir çekme isteği gönderin.

### Lisans

Bu proje MIT Lisansı altında lisanslanmıştır - detaylar için [LICENSE](LICENSE) dosyasına bakın.

---

Cloudflare DNS Güncelleyici ile DNS kayıtlarınızı yönetmek hiç bu kadar kolay olmamıştı. Güncellemelerinizi otomatikleştirin ve alan adlarınızın her zaman doğru şekilde yapılandırıldığından emin olun, kesinti ve manuel müdahaleyi en aza indirin.
