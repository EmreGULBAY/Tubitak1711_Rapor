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

  ![image](https://github.com/user-attachments/assets/ba79eb22-f4aa-49b8-b8a2-25ff94004963)
  <br>
  <em>Statsmodel.seasonal_decompose methonunun 365 günlük penceresinin residual sonucu</em>

  ![image](https://github.com/user-attachments/assets/68c1f02c-6698-4158-b097-1175563d9798)
  <br>
  <em>Verilerin 7 günlük hareketli ortalaması</em>

