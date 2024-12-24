<h1 align=center><font size = 6>Kasırga Sonrası Yapıların Sınıflandırılması</font></h1>

<img  src="https://raw.githubusercontent.com/geoaihub/geoaihub/main/assets/Mersin%20GeoAI%20Hub%202.png"  height=400  width=1000  alt="https://github.com/geoaihub"/>  

<small>Picture Source: <a  href="https://github.com/geoaihub">GeoAI Hub Mersin</a></small>

<br>

## Proje Hakkında

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

## Sonuçlar

- **Doğruluk:** Model, test verisinde yüksek doğruluk oranlarına ulaşmıştır.
- **CAMs Görselleştirme:** Modelin odaklandığı alanlar haritalandırılmıştır.

<br>

## Katkıda Bulunun

Bu projelere katkıda bulunmak için pull request gönderebilir veya issue açabilirsiniz.

<br>

## Lisans

Bu projeler, MIT lisansı altında yayınlanmıştır.
