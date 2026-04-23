# İris Veri Seti ile Karar Ağacı Sınıflandırması

Bu proje, Machine Learning (Makine Öğrenmesi) temel kavramlarını ve sınıflandırma algoritmalarından biri olan **Karar Ağaçları**nı (Decision Tree Classifier) pratik bir şekilde uygulamayı amaçlamaktadır. Projede, makine öğrenmesi eğitimlerinde sıklıkla tercih edilen meşhur **İris Veri Seti** kullanılmıştır.

##  Projenin Amacı
İris çiçeklerinin taç (petal) ve çanak (sepal) yaprak ölçülerine bakarak, çiçeğin 3 farklı İris türünden (Setosa, Versicolor, Virginica) hangisine ait olduğunu tahmin eden bir model geliştirmek ve bu modelin nasıl karar verdiğini görselleştirmektir.

## 🛠️ Kullanılan Teknolojiler ve Kütüphaneler
Proje Python programlama dili ile geliştirilmiş olup veri analizi, makine öğrenmesi ve görselleştirme için aşağıdaki kütüphaneler kullanılmıştır:
- **Pandas**: Veri manipülasyonu ve DataFrame işlemleri
- **Scikit-Learn (sklearn)**: Makine öğrenmesi modelleri oluşturma ve metrik hesaplamaları
- **Matplotlib & Seaborn**: Veri ve sonuç görselleştirme (Karmaşıklık Matrisi ve Karar Ağacı çizimleri)

##  Veri Seti Hakkında
**İris Veri Seti**, Scikit-Learn kütüphanesi içerisinde gömülü olarak gelmektedir. Set içerisinde 150 adet örnek ve 4 adet özellik (feature) bulunmaktadır:
1. Sepal Length (Çanak Yaprak Uzunluğu - cm)
2. Sepal Width (Çanak Yaprak Genişliği - cm)
3. Petal Length (Taç Yaprak Uzunluğu - cm)
4. Petal Width (Taç Yaprak Genişliği - cm)

Hedef değişken (Target), bu ölçülere dayanarak çiçeğin türünü ifade eden sınıflardır (0: Setosa, 1: Versicolor, 2: Virginica).

##  Model Geliştirme Süreci
1. **Veri Hazırlığı:** İris veri seti yüklenerek bir Pandas Dataframe'e aktarıldı. Özellikler (X) ve hedef değişken (y) olarak ayrıldı.
2. **Eğitim ve Test Bölünmesi:** Veri seti `train_test_split` ile %80 eğitim, %20 test verisi olacak şekilde (random_state=42) ikiye bölündü.
3. **Model Eğitimi:** `DecisionTreeClassifier` (criterion="gini", max_depth=3, random_state=42) oluşturularak eğitim verileriyle eğitildi.
4. **Tahmin (Prediction):** Ayrılan test verileri de modele verilerek tahminler elde edildi.

## Performans Değerlendirmesi
Modelin performansı test verisi üzerinde ölçüldüğünde elde edilen sonuçlar aşağıdaki gibidir:

- **Accuracy (Doğruluk Oranı):** `1.0` (%100 Başarı)
- **Karmaşıklık Matrisi (Confusion Matrix):** Test setindeki tüm sınıflar eksiksiz ve hatasız bir şekilde doğru tahmin edilmiştir. Seaborn kütüphanesi ile bir Isı Haritası (Heatmap) olarak görselleştirilmiştir.

##  Karar Ağacı Görselleştirmesi
Modelin arka planda kararları nasıl aldığı, hangi parametrelere göre bölme işlemi (split) uyguladığı Scikit-learn içerisindeki `plot_tree` fonksiyonu yardımıyla detaylı ve renklendirilmiş bir ağaç şeması olarak proje içerisinde sunulmuştur.




