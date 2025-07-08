# Ses Verisine Dayalı Lehçe Tanıma ve Öneri Sistemi: MFCC ve Web Tabanlı Makine Öğrenmesi Yaklaşımı

Bu projede, kullanıcıdan alınan ses kaydı üzerinden MFCC (Mel-Frequency Cepstral Coefficients) öznitelikleri çıkarılarak, kullanıcının olası beğeni veya ilgi alanlarının tahmin edilmesi hedeflenmiştir.
Elde edilen özellikler makine öğrenmesi modeline verilerek öneri sistemi alt yapısı oluşturulmuştur. Aynı zamanda mikrofon ile ses kaydı alınabilmekte ve Flask ile temel bir API sağlanmaktadır.

# Kullanılan Teknolojiler ve Kütüphaneler:
Python
Librosa – Ses sinyallerinden MFCC öznitelikleri çıkarma
NumPy – Sayısal işlemler ve veri saklama
Pandas – Veri seti okuma ve işleme
Scikit-learn – Modelleme (Random Forest)
Sounddevice & Wavio – Mikrofonla ses kaydı alma
Matplotlib – Öznitelik görselleştirme
Flask – Basit bir web arayüzü/API geliştirme

# PROJE AŞAMALARI
# 1- Veri Hazırlama: .tar arşivinden ses dosyaları çıkarılır. train.tsv dosyasından ses dosyası yolları ve etiketler (accent veya kategori) alınır.
# 2 - Öznitelik Çıkarımı: Her ses dosyasından MFCC öznitelikleri çıkarılır. Zaman boyutundaki ortalaması alınarak sabit boyutlu vektör elde edilir. Örnekleme hızı (sample rate) olarak 44100 Hz kullanılır.
# 3- Model Eğitimi: MFCC öznitelikleri ile etiketler eşleştirilir. RandomForestClassifier ile model eğitimi yapılır. Model doğruluğu: %82 (accuracy = 0.824)
# 4- Ses Kaydı: Kullanıcıdan mikrofon aracılığıyla ses kaydı alınır. .wav formatında kaydedilir, analiz için hazır hale getirilir.
# 5 - API Geliştirme: Flask ile temel bir web arayüzü sağlanır. İleride ses yollayıp sınıflandırma sonucunu almak için API genişletilebilir.

# Dosya Yapısı:
├── extracted_features.npy       # Kaydedilen MFCC vektörleri
├── voiceDatas.tar               # Sıkıştırılmış ses verisi
├── extracted_files/             # Açılmış ses dosyaları ve .tsv dosyaları
├── train.tsv                    # Etiketli veri seti
├── recorded_audio.wav           # Mikrofonla alınan ses
├── app.py                       # Flask web uygulaması
├── model_training.py            # Eğitim ve modelleme kodu
└── README.md

# Geliştirme Önerileri : 
Modeli derin öğrenme ile güçlendirmek (CNN, LSTM). Öneri sistemini daha fazla kullanıcı verisi ile zenginleştirmek.

# Proje Sahibi
Çağdaş ÇANKAYA
