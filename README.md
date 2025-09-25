# 🌱 Bitki Sağlık Durumu Sınıflandırma (CNN Projesi)

Bu proje, yapay sinir ağları (Convolutional Neural Networks - CNN) kullanarak bitki yapraklarının **sağlıklı** veya **sağlıksız** olduğunu tespit etmeye yönelik bir denemedir.  
Amacım, temel bir derin öğrenme modeliyle bilgisayarla görme (computer vision) üzerine pratik yapmak ve öğrenme sürecimi belgelemekti.

---

## 🚀 Kullanılan Teknolojiler
- Python, NumPy, Pandas, Matplotlib, Seaborn  
- OpenCV (görüntü işleme için)  
- TensorFlow & Keras (modelleme için)  
- scikit-learn (değerlendirme metrikleri için)  

---

## 📂 Veri Seti
- Toplam **707 görüntü** kullanıldı.  
  - **326 sağlıklı** yaprak  
  - **381 sağlıksız** yaprak  
- Görseller aynı boyuta (224x224) getirildi.  

---

## 🧠 Model Mimarisi
- 3 adet **Conv2D + MaxPooling + BatchNormalization** bloğu  
- Dropout katmanları ile aşırı öğrenme (overfitting) engellenmeye çalışıldı  
- Flatten → Dense(512) → Dense(128) → Çıkış katmanı (Sigmoid aktivasyon)  

---

## 🎯 Eğitim
- Kayıp fonksiyonu: **Binary Crossentropy**  
- Optimizasyon: **Adam (lr=0.0005)**  
- Erken durdurma ve en iyi modeli kaydetme callback’leri kullanıldı.  

---

## 📊 Sonuçlar
- Eğitim sürecinde model belli bir doğruluk oranına ulaşsa da **validation accuracy düşük kaldı**.  
- Model, bazı durumlarda **sağlıklı ve sağlıksız yaprakları ayırt etmekte zorlandı**.  
- Bu durumun muhtemel sebepleri:  
  - Veri setinin görece küçük olması  
  - Görsellerdeki çeşitliliğin sınırlı kalması  
  - Modelin karmaşık örüntüleri yakalamakta yetersiz kalması  

---

## 💡 Geliştirme Fikirleri
- Daha büyük ve dengeli bir veri seti ile yeniden deneme  
- Veri artırma (data augmentation) tekniklerinin yoğunlaştırılması  
- Transfer learning (örneğin, **ResNet50, EfficientNet**) ile önceden eğitilmiş modellerden faydalanma  
- Hiperparametre optimizasyonu  

---

## 🙋🏻‍♂️ Kapanış
Bu proje benim için güzel bir öğrenme deneyimi oldu.  
Model şu an **mükemmel sonuçlar vermese de**, sürecin bana kazandırdığı deneyim çok değerliydi.  
Bir sonraki adımda transfer learning yöntemlerini denemeyi planlıyorum.  
