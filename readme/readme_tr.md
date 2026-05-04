# 🎬 Bilibili Video Analiz Aracı

> Bilibili'den video içeriği çıkarmak için hafif, hızlı ve çok yönlü bir araç (Eğitim & Araştırma Sürümü)

[🌐 Çevrimiçi Demo](https://twittervideodownloaderx.com/bilibili_downloader_tu) • [📝 Kullanım Kılavuzu](#-kullanım-kılavuzu) • [❓ Sıkça Sorulan Sorular](#-sıkça-sorulan-sorular)

---

## 📋 Proje Genel Bakışı

Bu proje, Bilibili platformundaki (哔哩哔哩) herkese açık videolardan medya kaynakları meta verilerini güvenli bir şekilde çıkarmak ve çeşitli formatlarda dönüştürme/yerel kaydetme seçeneği sunmak amacıyla geliştirilmiş web tabanlı bir video analiz aracıdır. Herhangi bir istemci yazılım kurulumu veya hesap kaydı gerektirmez; doğrudan tarayıcınız üzerinden kullanabilirsiniz.

> ⚠️ **Önemli Uyarı**: Bu araç yalnızca kişisel öğrenme, teknik araştırma ve makul kullanım sınırları içinde kullanılmak üzere tasarlanmıştır. Lütfen [Bilibili Topluluk Kuralları](https://www.bilibili.com/blackboard/protocol.html), 《Çin Halk Cumhuriyeti Telif Hakkı Kanunu》 ve diğer geçerli düzenlemelere uyun. Yaratıcıların emeğine saygı gösterin; indirilen içeriği ticari amaçlarla veya başkalarının haklarını ihlal edecek şekilde kullanmayın.

---

## ✨ Temel Özellikler

- 🔗 **Bağlantı Analizi**: Standart Bilibili video/animasyon URL'lerini destekler; bölümleri ve mevcut çözünürlük seçeneklerini otomatik olarak tanır
- 📥 **Çoklu Format Dışa Aktarma**:
  - Orijinal video akışı (1080P/720P gibi herkese açık çözünürlükleri destekler)
  - Ses çıkarma → MP3 formatı (dersleri/müziği çevrimdışı dinlemek için pratik)
  - Video klibi → Animasyonlu GIF'e dönüştürme (meme oluşturma/eğitim demostrasyonları için ideal)
- 🌍 **Çok Dilli Arayüz**: Türkçe, İngilizce, Çince, Japonca, Korece ve daha fazla dil desteği
- 📱 **Çapraz Platform Uyumluluğu**: Chrome / Firefox / Safari / Edge tarayıcılarında sorunsuz çalışır; mobil cihazlar ve tabletler için optimize edilmiş deneyim
- 🔒 **Gizlilik Öncelikli**: Bilibili hesabı girişi gerekmez, kişisel veri toplanmaz; analiz süreci tamamen anonimdir
- ⚡ **Hızlı İşleme**: Analiz ortalama 5-10 saniyede tamamlanır; eşzamanlı istekler ve toplu işlem desteği

---

## 🚀 Hızlı Başlangıç

### Çevrimiçi Kullanım (önerilen)
1. [https://twittervideodownloaderx.com/bilibili_downloader_tu](https://twittervideodownloaderx.com/bilibili_downloader_tu) adresine gidin
2. Hedef videonun bağlantısını kopyalayın (örnek: `https://www.bilibili.com/video/BV1xx411c7mD`)
3. Bağlantıyı giriş alanına yapıştırın → 「Analiz Et」butonuna tıklayın
4. İstediğiniz çözünürlük ve formatı seçin → Tarayıcı talimatlarını izleyerek dosyayı kaydedin

### Yerel Dağıtım (geliştiriciler için)
```bash
# Deposu klonlayın
git clone https://github.com/your-repo/bili-video-parser.git

# Bağımlılıkları yükleyin
cd bili-video-parser && npm install

# Ortam değişkenlerini yapılandırın (isteğe bağlı)
cp .env.example .env

# Geliştirme sunucusunu başlatın
npm run dev
```

> 💡 Not: Bu proje Node.js + Express tabanlı bir mimari kullanır. Ayrıntılı dağıtım belgeleri için `/docs/DEPLOY.md` dosyasına bakınız.

---

## 🛠 Teknoloji Yığını

| Modül | Kullanılan Teknolojiler |
|-------|-------------------------|
| Ön Yüz | Vue 3 + TypeScript + Vite |
| Arka Yüz | Node.js + Express + Axios |
| Video İşleme | ffmpeg.wasm (hafif istemci tarafı dönüştürme) |
| Proxy Yönlendirme | Cloudflare Workers / Özel Ara Katman Yazılımı |
| Uluslararasılaştırma | vue-i18n + JSON Dil Paketleri |

---

## 📚 Kullanım Kılavuzu

### Temel Çalışma Akışı
```
1. Video bağlantısını alın
   └─ Bilibili'de hedef videoyu açın → Tarayıcı adres çubuğundan URL'yi kopyalayın

2. Analiz isteği gönderin
   └─ Bağlantıyı araç giriş alanına yapıştırın → 「Analizi Başlat」butonuna tıklayın

3. Çıktı yapılandırmasını seçin
   ├─ 🎬 Video İndir: Çözünürlük seçin (360P/720P/1080P vb. - yalnızca herkese açık seçenekler)
   ├─ 🎵 Ses Çıkar: MP3 dosyası oluştur (dersleri/müziği çevrimdışı dinlemek için ideal)
   └─ 🎞 GIF Oluştur: Belirtilen zaman aralığından animasyon oluştur (önerilen: ≤15 saniye)

4. Dosyayı kaydedin
   └─ Kaynak yeni sekmede açılacak → Sağ tık/menü → 「Farklı kaydet」
```

### Mobil Cihazlarda Kullanım İpuçları
- iOS Safari: Paylaş butonu → 「Dosyalara Kaydet」
- Android Chrome: Video önizlemesine basılı tutun → 「Video indir」
- Video otomatik oynatılıyorsa: Oynatıcı sağ üst köşedeki `⋮` simgesine tıklayın → 「İndir」seçeneğini seçin

---

## ❓ Sıkça Sorulan Sorular

**S: İndirilen dosyalar nereye kaydedilir?**  
C: Dosyalar, tarayıcınızda yapılandırılan indirme klasörüne kaydedilir. Bu yolu tarayıcı ayarlarından kontrol edebilir veya değiştirebilirsiniz.

**S: Üyelere özel veya giriş gerektiren içeriği analiz edebilir miyim?**  
C: Hayır. Bu araç yalnızca herkese açık olarak ayarlanmış videolarla çalışır ve orijinal içeriğin erişim ayarlarına saygı duyar.

**S: Dönüştürme sonrası görüntü/ses kalitesi düşer mi?**  
C: Video indirmeleri, seçilen çözünürlüğün orijinal bit hızını korur. MP3 formatı 128 kbps standart kodlama kullanır. GIF formatı ise dosya boyutu ve akıcılık arasında denge kurmak için süreye göre kare hızını optimize eder.

**S: İndirme geçmişi veya önbellek saklanır mı?**  
C: Hayır. Tüm kaynaklar geçici bir proxy aracılığıyla doğrudan kullanıcının cihazına iletilir; sunucu herhangi bir istek veya medya dosyası saklamaz.

**S: Analiz başarısız olursa ne yapmalıyım?**  
C: Lütfen şunları kontrol edin: ① Bağlantının geçerli bir herkese açık videoya ait olup olmadığı ② İnternet bağlantınızın stabil olup olmadığı ③ Farklı bir tarayıcı deneyin. Sorun devam ederse, bir Issue açarak bildirmekten çekinmeyin.

---

## ⚖️ Yasal Uyumluluk ve Sorumluluk Reddi

- Bu araç, platformların **hiçbir teknik koruma önlemini atlamaz veya ihlal etmez**; yalnızca genel arayüzler aracılığıyla meta verileri alır
- Kullanıcı, kendi kullanımının yerel yasalara ve platformun hizmet şartlarına uygun olduğunu doğrulamaktan sorumludur
- Önerilen kullanım senaryoları: Kişisel öğrenme arşivleme, eğitim amaçlı gösterimler, içerik oluşturma için referans materyaller... her zaman adil kullanım (Fair Use) çerçevesinde
- Hak ihlali şüphesi taşıyan bir içerik fark ederseniz, lütfen [Bilibili'nin bu telif hakkı bildirim formu aracılığıyla](https://www.bilibili.com/blackboard/help.html#copyright) resmi kanala başvurun

---

## 🤝 Katkı Sağlama Kılavuzu

Pull Request'lerinizi ve Issue bildirimlerinizi memnuniyetle karşılıyoruz! Katkı sağlamadan önce lütfen aşağıdaki belgeleri inceleyin:
- [Kod Standartları](/CONTRIBUTING.md)
- [Çok Dilli Çeviri Kılavuzu](/locales/README.md)
- [Güvenlik ve Uyumluluk Gereksinimleri](/SECURITY.md)

---

## 📄 Lisans

Bu proje [MIT Lisansı](/LICENSE) altında yayınlanmaktadır. Eğitim ve araştırma amaçlı ücretsiz olarak kullanılabilir. Ticari kullanım için, lütfen geçerli yasal düzenlemelere uyumu dikkatlice kontrol ediniz.

---

> 🌟 Bu araç sizin için faydalı olduysa, ✨bir Yıldız (Star) vermeyi unutmayın! Desteğiniz, bu projeyi sürdürmeye ve geliştirmeye devam etmemiz için en büyük motivasyon kaynağıdır~

*Son güncelleme: Mayıs 2026 | Sürüm: v1.0.0*