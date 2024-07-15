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
    ![image](https://github.com/user-attachments/assets/ba79eb22-f4aa-49b8-b8a2-25ff94004963)
    <br>
    <em >Statsmodel.seasonal_decompose methonunun 365 günlük penceresinin residual sonucu</em>
  </p>
  
  
  <p align="center">
    ![image](https://github.com/user-attachments/assets/064be28f-17d2-44f1-b62f-30b9ec0ab1f7)
    <br>
    <em>Verilerin 7 günlük hareketli ortalaması</em>
  </p>
