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
- Veriler ayrıca hareketli ortalama yöntemi ile sezonsallıktan ayırıldı ve testler sonucunda hangi yöntemin en iyi sonuç verdiğine karar verildi.

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
