<h1 align=center><font size = 6>Kasırga Sonrası Yapıların Sınıflandırılması</font></h1>

<img  src="https://raw.githubusercontent.com/geoaihub/geoaihub/main/assets/Mersin%20GeoAI%20Hub%202.png"  height=400  width=1000  alt="https://github.com/geoaihub"/>  

<small>Picture Source: <a  href="https://github.com/geoaihub">GeoAI Hub Mersin</a></small>

<br>

## Proje Hakkında

Hurricane Harvey, 25 Ağustos 2017 tarihinde Karaipler’den başlayarak, Amerika Birleşik Devletleri'nin güneydoğu kıyısında büyük hasara yol açan, şiddetli bir tropikal fırtına ve kasırgadır. Kasırga, özellikle Texas ve Louisiana eyaletlerini etkileyerek tarihteki en yıkıcı doğal afetlerden birine neden olmuştur. Harvey, tam anlamıyla bir "çoklu afet" durumu yaratmış, şiddetli rüzgarlar, yoğun yağışlar ve büyük sel baskınlarıyla birlikte bölgedeki birçok yapıyı tahrip etmiştir. Kasırga, Houston gibi büyük şehirlerde ciddi altyapı hasarlarına yol açmış, binlerce bina hasar görmüş ve çok sayıda insan evsiz kalmıştır. Yağışlar, bölgedeki su seviyelerinin hızla yükselmesine ve geniş çaplı sel felaketlerine neden olmuştur. Bu nedenle, Harvey'nin ardından yapılan hasar tespiti çalışmaları, özellikle uydu görüntülerinden faydalanarak, kasırganın etkilerini hızlı ve doğru bir şekilde değerlendirme amacı taşımaktadır.

Bu proje, Hurricane Harvey sonrası uydu görüntülerindeki yapı hasarlarını sınıflandırmak için VGG-16 derin öğrenme mimarisini kullanmaktadır. Modelin odaklandığı bölgeler, Class Activation Maps (CAMs) yöntemiyle görselleştirilmiştir.

<br>

## Yöntemler

### VGG-16

VGG-16, derin öğrenme alanında yaygın olarak kullanılan bir görüntü sınıflandırma modelidir. Model, 13 konvolüsyonel ve 3 tam bağlantılı katmandan oluşur. Küçük filtre boyutları (3x3) kullanarak detaylı özellikleri öğrenir. Bu mimari, transfer öğrenme için uygundur ve önceden eğitilmiş ağırlıklarla kullanılabilir.

- **Hedef:** Kasırga sonrası hasar görmüş ve hasar görmemiş yapıları sınıflandırmak.
- **Avantajlar:**
  - Derin öğrenme tabanlı mimari.
  - Transfer öğrenme ile önceden eğitilmiş ağırlıkları kullanma.
  - Daha az veri ile yüksek performans sağlama.
- **Değerlendirme Metrikleri:**
  - Doğruluk (Accuracy)
  - Hassasiyet (Precision)
  - Duyarlılık (Recall)

### Class Activation Maps (CAMs)

Class Activation Maps, modelin karar verirken hangi görüntü bölgelerine odaklandığını görselleştirir. Bu yöntem, modelin karar süreçlerini şeffaf hale getirir ve kullanıcıların modelin hangi özelliklere dikkat ettiğini anlamasına olanak tanır.

- **Hedef:** Modelin hangi bölgelere odaklandığını göstermek.
- **Avantajlar:**
  - Model kararlarının daha iyi anlaşılması.
  - Hasarın yoğun olduğu alanların görselleştirilmesi.
 
### Model Çıktı Görselleştirmesi

Aşağıdaki görsel, modelin kasırga sonrası hasar sınıflandırması üzerindeki performansını ve karar mekanizmasını göstermektedir:

1. **Orijinal Görüntü:** Modelin giriş olarak kullandığı uydu görüntüsü.
2. **Üst Üste Bindirilmiş Görüntü:** Modelin odaklandığı alanların ısı haritası ile görselleştirilmesi.
3. **Class Activation Map (CAM):** Modelin dikkate aldığı bölgeleri gösteren saf ısı haritası.

<img  src="https://raw.githubusercontent.com/geoaihub/GeoTalks/refs/heads/main/Scene%20Classification/plots/damage_1.png"  height=400  width=1000  alt="https://github.com/geoaihub"/> 

Model, bu görüntüdeki hasar olasılığını **%99.99** olarak tahmin etmiştir.


## Sonuçlar

Sonuçlar, modelin test verisi üzerinde yüksek doğruluk oranlarına ulaşarak sınıflandırma performansını başarılı bir şekilde kanıtladığını göstermektedir. Hasar tespitinde özellikle kritik bölgelerde doğru tahminler yapılmış ve modelin güvenilirliği sağlanmıştır. Modelin karar mekanizmasını daha iyi anlayabilmek için Class Activation Maps (CAMs) görselleştirmeleri kullanılmıştır. Bu görseller, modelin hasar tespiti yaparken odaklandığı bölgeleri net bir şekilde ortaya koymaktadır. Kırmızı renklerle işaretlenen alanlar, modelin hasar olduğuna dair en güçlü kanıtları bulduğu bölgeleri temsil etmektedir. Bu sayede, modelin güvenilirliği ve şeffaflığı daha da artırılmıştır.

<br>

## Katkıda Bulunun

Bu projelere katkıda bulunmak için pull request gönderebilir veya issue açabilirsiniz.

<br>

## Lisans

Bu projeler, MIT lisansı altında yayınlanmıştır.
