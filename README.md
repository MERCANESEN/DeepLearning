Projenin Amacı
Bu proje, savaş ve normal fotoğrafları birbirinden ayırmak için bir derin öğrenme modeli geliştirmeyi amaçlamaktadır. Özellikle, TensorFlow ve Keras kullanılarak eğitimli bir MobileNetV2 modeli üzerine inşa edilen bu model, savaş içeren fotoğrafları tanımlamayı ve ayırmayı hedefler. Projenin nihai amacı, savaş durumlarının otomatik tespit edilmesi ve analiz edilmesine yardımcı olmaktır.

Kullanılan Veri Setleri
Proje kapsamında iki farklı sınıfa ait toplamda 4000 fotoğraf kullanılmıştır:

Normal Fotoğraflar: 2000 adet
Savaş Fotoğrafları: 2000 adet
Bu veri seti, eğitim, doğrulama ve test aşamaları için belirli oranlarda bölünmüştür:

Kullanılan Model ve Mimariler
MobileNetV2: Hafif ve hızlı bir derin öğrenme mimarisi olup, mobil ve gömülü cihazlar için optimize edilmiştir. Model, ImageNet veri seti üzerinde önceden eğitilmiş ağırlıklarla kullanılmış ve yalnızca özellik çıkarım katmanları kullanılmıştır.
Ek Katmanlar:
GlobalAveragePooling2D: Uzaysal boyutları ortalama alarak sıkıştıran bir katman.
Dense Layer: Sigmoid aktivasyon fonksiyonu ile tek bir nörona sahip tam bağlantılı katman.
Temel Bulgular
Doğruluk (Accuracy): Eğitim ve doğrulama doğruluğu zamanla yüksek seviyelere ulaşmıştır. Model, eğitim ve doğrulama setlerinde benzer doğruluk oranları göstererek aşırı öğrenme yapmadığını göstermiştir.
Kayıp (Loss): Eğitim ve doğrulama kayıpları zamanla azalmış ve benzer eğilimler göstermiştir.
Karışıklık Matrisi: Model, normal ve savaş fotoğraflarını büyük ölçüde doğru sınıflandırmıştır. Yanlış sınıflandırmalar az sayıda olup, genel doğruluğun yüksek olduğunu işaret eder.
Performans Özeti
Eğitim ve Doğrulama Doğruluğu: Eğitim ve doğrulama doğruluğu 30 epoch sonunda yaklaşık %90'ın üzerine çıkmıştır.
Eğitim ve Doğrulama Kayıp: Eğitim ve doğrulama kayıpları 0.2 seviyesinin altına inmiştir.
Karışıklık Matrisi: Model, 197 normal ve 146 savaş fotoğrafını doğru sınıflandırmıştır. Yanlış sınıflandırmalar, 9 normal fotoğrafı savaş olarak ve 17 savaş fotoğrafını normal olarak sınıflandırmıştır.
Sonuç
Bu proje, savaş ve normal fotoğrafları etkili bir şekilde ayırt edebilen bir derin öğrenme modeli geliştirmiştir. Model, eğitim ve doğrulama aşamalarında yüksek doğruluk ve düşük kayıp oranları göstermiştir. Gelecekte, modelin performansını daha da artırmak için veri artırma ve regularization teknikleri kullanılabilir. Bu model, savaş durumlarının otomatik tespit edilmesi ve analiz edilmesi gibi pratik uygulamalarda kullanılabilir.
