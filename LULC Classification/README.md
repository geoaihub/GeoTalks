<h1 align=center><font size = 6>Sentinel-2 ile LULC Sınıflandırma</font></h1>

<img  src="https://raw.githubusercontent.com/geoaihub/geoaihub/main/assets/Mersin%20GeoAI%20Hub%202.png"  height=400  width=1000  alt="https://github.com/geoaihub"/>  

<small>Picture Source: <a  href="https://github.com/geoaihub">GeoAI Hub Mersin</a></small>

<br>

## Proje Hakkında
Bu proje, Sentinel-2 uydu görüntülerinden elde edilen spektral bantlar ve türetilmiş indeksler kullanılarak Çukurova Havzası'nın arazi örtüsü ve arazi kullanımı sınıflandırmasını gerçekleştirmektedir. Projede, rastgele orman (Random Forest) algoritması ve açıklanabilir yapay zeka yöntemleri (örneğin, SHAP) uygulanmıştır.

<br>

## Veri Seti
- **Kaynak:** Sentinel-2 uydu görüntüleri.
- **İçerik:** 
  - 9 spektral bant (örneğin, B2, B3, B4, B8).
  - 9 indeks (örneğin, NDVI, NDWI, NDTI).
  - Sayısal Yükseklik Modeli (SYM).
- **Etiketli Veriler:** Toplamda 1.575.249 piksel etiketlenmiş ve her sınıf için yaklaşık 20.000 etiketli nokta kullanılmıştır.

<br>

## Kullanılan Yöntemler
### Rastgele Orman (Random Forest)
- **Hiperparametreler:** 
  - `max_depth`: 30
  - `min_samples_leaf`: 1
- **Değerlendirme Metrikleri:**
  - Doğruluk
  - F1 Skoru
  - Kappa
- **Özellik Önem Dereceleri:** Modelin hangi özelliklere daha fazla önem verdiği SHAP ile analiz edilmiştir.

### SHAP (SHapley Additive Explanations)
SHAP yöntemi, sınıflandırma modelinin karar süreçlerini açıklamak için kullanılmıştır. Bu yöntemle, her bir özelliğin sınıflandırma üzerindeki etkisi görselleştirilmiştir.

<br>

## Çıktılar
- **Karışıklık Matrisi:** Modelin hangi sınıflar arasında hata yaptığı analiz edilmiştir.
- **SHAP Değerleri:** Özelliklerin önem dereceleri grafiklerle gösterilmiştir.
- **Haritalama:** Sınıflandırma sonuçları coğrafi haritalar üzerinde görselleştirilmiştir.
 
<br>

## Katkıda Bulunun
Bu projeye katkıda bulunmak için lütfen bir **pull request** gönderin veya bir **issue** açarak görüşlerinizi paylaşın.

<br>

## Lisans

Bu projeler, MIT lisansı altında yayınlanmıştır.
