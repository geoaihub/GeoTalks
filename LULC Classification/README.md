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
- **Etiketli Veriler:** 5 farklı sınıfta, her bir sınıf için 20.000 etiketli nokta kullanılmıştır.

<br>

## Kullanılan Yöntemler
### Rastgele Orman (Random Forest)

Random Forest, makine öğrenmesinde yaygın olarak kullanılan bir denetimli öğrenme algoritmasıdır. Birden fazla karar ağacının birleşiminden oluşan bir topluluk öğrenme (ensemble learning) yöntemidir. Her bir karar ağacı, verilen veriye göre sınıflandırma veya regresyon tahminleri yapar. Random Forest, bu bireysel ağaçların tahminlerini birleştirerek daha doğru ve güvenilir sonuçlar elde eder.

- **Hiperparametreler:** 
  - `max_depth`: 30
  - `min_samples_leaf`: 1
- **Değerlendirme Metrikleri:**
  - Doğruluk
  - F1 Skoru
- **Özellik Önem Dereceleri:** Modelin hangi özelliklere daha fazla önem verdiği SHAP ile analiz edilmiştir.

<br>

### SHAP (SHapley Additive Explanations)
SHAP yöntemi, sınıflandırma modelinin karar süreçlerini açıklamak için kullanılmıştır. Bu yöntemle, her bir özelliğin sınıflandırma üzerindeki etkisi görselleştirilmiştir.

Daha spesifik olmak gerekirsek eğer, bu çalışmada beş farklı arazi sınıfına ait global minimum ve maksimum değerler belirlenerek SHAP değerleri görselleştirilmiştir. İlk olarak, her bir sınıf için SHAP değerleri yüklenip yeniden şekillendirilerek 50x50'lik bir matris oluşturulmuştur. Ardından, bu verilerin 32x32'lik kısmı kullanılarak her sınıf için renkli haritalar (heatmap) oluşturulmuştur. Görselleştirme, her bir sınıfın model üzerindeki etkisini göstermek amacıyla SHAP değerlerini renkli bir şekilde sunmuştur. Sonuç olarak, bu işlem, modelin hangi özelliklere odaklandığını ve karar verme süreçlerini daha şeffaf hale getirmiştir.

<img  src="https://raw.githubusercontent.com/geoaihub/GeoTalks/refs/heads/main/LULC%20Classification/plots/SHAP_visual.png"  height=300  width=1000  alt="https://github.com/geoaihub"/>

<br>

## Çıktılar

Bu çalışmada, modelin performansı çeşitli yöntemlerle analiz edilmiştir. İlk olarak, karışıklık matrisi kullanılarak modelin hangi sınıflar arasında hata yaptığı incelenmiştir. Ardından, SHAP değerleri ile modelin kullandığı özelliklerin önem dereceleri grafiksel olarak gösterilmiştir. Son olarak, haritalama yöntemiyle, sınıflandırma sonuçları coğrafi haritalar üzerinde görselleştirilerek, modelin tahminlerinin mekansal dağılımı ortaya konulmuştur.
 
<br>

## Katkıda Bulunun
Bu projeye katkıda bulunmak için lütfen bir **pull request** gönderin veya bir **issue** açarak görüşlerinizi paylaşın.

<br>

## Lisans

Bu projeler, MIT lisansı altında yayınlanmıştır.
