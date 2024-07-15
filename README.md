# Tubitak1711_Rapor

## 1 - Kütüphaneler

- numpy: matematiksel operasyonlar.
- pandas: veri analizi.
- matplotlib: veri görselleştrime.
- plotly: etkileşimli veri görselleştirme.
- sklearn: makine öğrenmesi algoritmaları ve verileri ölçekleme.
- statsmodels: istatistiksel model tahmini.

## 2 - Verlerin Hazırlanması

- Anlaşmalı otellerin sağladığı verilerin 2022, 2023 ve 2024 verilerinin günlük harcanan elektrik, doluluk ve hissedilen hava sıcaklığı kısımları seçildi.
- 3 yılın verisi birleştirildi.
- 2021 ve öncesi verileri Covid dönemi nedeniyle atlandı.
- Statsmodel kütüphanesinin ilgili modülü (seasonal_decompose) kullanılarak sezonsallıktan ayırıldı.
- Veriler ayrıca hareketli ortalama yöntemi ile sezonsallıktan ayırıldı.
- Testler sonucunda 7 günlük hareketli ortalamanın en iyi sonucu verdiğine karar verildi.
- Oluşan normal sonucu otelin doluluğuna günlük olarak otel doluluğuna bölerek kişi başına düşen elektrik tüketimi elde edildi.

  <p align="center">
    <img src="images/Ekran görüntüsü 2024-07-15 163510.png">
    <br>
    <em >Statsmodel.seasonal_decompose methonunun 365 günlük penceresinin residual sonucu</em>
  </p>
  
  <p align="center">
    <img src="images/Ekran görüntüsü 2024-07-15 163701.png">
    <br>
    <em>Verilerin 7 günlük hareketli ortalaması</em>
  </p>

  <p align="center">
    <img src="images/Ekran görüntüsü 2024-07-15 164836.png">
    <br>
    <em>7 günlük hareketli ortalamanın kişi başına düşen elektrik miktarı</em>
  </p>

## 3 - Anomali Tespit Yöntemleri

### 3.1 - Isolation Forest

- Isolation Forest, anomalileri normal verilerden izole ederek tespit etmeye odaklanır. Bu yöntem, anormal veri noktalarının daha az sayıda bölünme gerektirmesi nedeniyle daha kısa yollarla izole edilebileceği varsayımına dayanır.
- Büyük veri setlerinde dahi hızlı ve verimli çalışır. Bu, özellikle yüksek boyutlu ve büyük hacimli veri setleriyle çalışırken önemlidir.
- Modelin nasıl çalıştığı ve karar verme süreçleri, diğer bazı karmaşık algoritmalara kıyasla daha kolay anlaşılır ve açıklanabilir.
- Veri setindeki gürültü veya hatalı veri noktaları, Isolation Forest algoritmasının performansını önemli ölçüde etkilemez. Bu da yöntemi daha güvenilir hale getirir.

  <p align="center">
    <img src="images/Ekran görüntüsü 2024-07-15 165443.png">
    <br>
    <em>Elde edilen verinin isolation forest algoritmasından geçirilmiş hali</em>
  </p>
  
