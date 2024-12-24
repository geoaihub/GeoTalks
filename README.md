<h1 align=center><font size = 6>GeoTalks: LULC Sınıflandırma ve Sahne Sınıflandırma Çalışmaları</font></h1>

<img  src="https://raw.githubusercontent.com/geoaihub/geoaihub/main/assets/Mersin%20GeoAI%20Hub%202.png"  height=400  width=1000  alt="https://github.com/geoaihub"/>  

<small>Picture Source: <a  href="https://github.com/geoaihub">GeoAI Hub Mersin</a></small>

<br>

## GeoTalks Hakkında
İstanbul Teknik Üniversitesi Jeodezi ve Fotogrametri Kulübü (JFK) tarafından düzenlenen [GeoTalks](https://jfk.itu.edu.tr/index.html), Geomatik Mühendisliği öğrencileri ile sektörde çalışan uzmanları bir araya getiren bir etkinlikler serisidir. Bu etkinliklerde mesleki deneyimler paylaşılır, katılımcılar farklı bakış açıları kazanır ve meslektaşlarıyla rahatça iletişim kurma fırsatı bulur. GeoTalks, online eğitim sürecinde başlatılmış olup, yüz yüze eğitimde de devam ettirilmektedir.

## Bu Repository Hakkında
Bu repository, GeoTalks etkinlikleri kapsamında gerçekleştirilen iki çalışmayı içermektedir:
1. **LULC (Arazi Örtüsü ve Kullanımı) Sınıflandırma** 
2. **Scene Classification (Kasırga Sonrası Yapıların Sınıflandırılması)**

<br>

### 1. LULC Sınıflandırma
Bu çalışmada, Sentinel-2 uydu görüntüleri ve türetilmiş indeksler (örneğin NDVI, NDWI, NDTI) kullanılarak Çukurova Havzası'nın arazi örtüsü ve arazi kullanımı sınıflandırılmıştır. Araştırma kapsamında hem geleneksel makine öğrenimi algoritmaları hem de açıklanabilir yapay zeka teknikleri uygulanmıştır.

#### Detaylar:
- **Veri Seti:** Çalışmada, 18 Ağustos 2023 tarihli Sentinel-2 uydu görüntülerinden elde edilen dokuz adet spektral bant ve dokuz adet indeks kullanılmıştır. Toplamda 1.575.249 piksel etiketlenmiş, eğitim için 100.000 etiketli nokta oluşturulmuştur.
- **Yöntem:** Rastgele orman (Random Forest) sınıflandırıcısı kullanılarak, modelin performansı doğruluk, F1 skoru ve Kappa metriği ile değerlendirilmiştir. Ayrıca, SHAP (SHapley Additive Explanations) yöntemiyle modelin karar süreçleri açıklanmıştır.
- **Amaç:** Arazi sınıflarını doğru bir şekilde tespit etmek ve sınıflandırma sürecindeki en etkili öznitelikleri belirlemek.
- **Sonuçlar:** Sınıflandırma sonuçları harita üzerinde görselleştirilmiş ve farklı arazi örtüsü türleri analiz edilmiştir.

Daha fazla bilgi ve kod için [buraya tıklayın](https://github.com/geoaihub/GeoTalks/tree/main/LULC%20Classification).

<br>

### 2. Sahne Sınıflandırma
Bu çalışmada, Hurricane Harvey sonrası uydu görüntüleri kullanılarak yapıların sınıflandırılması gerçekleştirilmiştir. Derin öğrenme tabanlı VGG-16 mimarisi kullanılmış ve Class Activation Maps (CAMs) yöntemiyle modelin karar süreçleri görselleştirilmiştir.

#### Detaylar:
- **Veri Seti:** Kaggle üzerinden temin edilen Hurricane Damage Satellite Images veri seti kullanılmıştır. Veri seti, kasırga sonrası hasar görmüş ve hasar görmemiş yapıları içermektedir.
- **Yöntem:** 
  - VGG-16 modeli, transfer öğrenme yöntemiyle eğitilmiştir. Modelin son katmanları, hasar sınıflarını sınıflandırmak için özelleştirilmiştir.
  - Eğitim sürecinde veri artırma teknikleri uygulanarak modelin genelleştirme yeteneği artırılmıştır.
  - Class Activation Maps (CAMs) ile modelin hangi görüntü bölgelerine odaklandığı görselleştirilmiştir.
- **Amaç:** Kasırga sonrası yapı hasarlarını doğru bir şekilde sınıflandırmak ve modelin karar süreçlerini açıklamak.
- **Sonuçlar:** Hasarlı ve hasarsız yapılar yüksek doğrulukla sınıflandırılmış, modelin dikkat ettiği bölgeler CAMs ile görselleştirilmiştir.

Daha fazla bilgi ve kod için [buraya tıklayın](https://github.com/geoaihub/GeoTalks/tree/main/Scene%20Classification).

<br>

## Katkıda Bulunun
Bu projeye katkıda bulunmak için lütfen bir **pull request** gönderin veya bir **issue** açarak görüşlerinizi paylaşın.

## Lisans
Bu repository, MIT lisansı altında yayımlanmıştır.
