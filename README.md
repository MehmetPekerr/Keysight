<<<<<<< HEAD
<<<<<<< HEAD
<<<<<<< HEAD
# 🎵 Keysight — AI-Powered Music Emotion & Tonality Analyzer

**Keysight**, MIDI formatındaki müzik dosyalarını yapay zeka kullanarak analiz eden ve müziğin tonalitesini (Major/Minor) ile yansıttığı duyguları tespit eden bir web uygulamasıdır.

> Piyano notalarından duygu çıkarımı yapan derin öğrenme modelleri + sezgisel bir web arayüzü.

---

## 🚀 Özellikler

- 🎹 **MIDI Dosya Analizi** — .mid / .midi formatındaki dosyaları yükleyip analiz et
- 🎼 **Tonalite Tespiti** — Major / Minor ayrımını otomatik belirle
- 💡 **Duygu Tahmini** — Neşe, Hüzün, Enerji, Melankoli, Heyecan, Endişe gibi 9 farklı duygu kategorisinde tahmin
- 📊 **Görsel Raporlama** — Tahmin sonuçlarını 4 farklı grafik ile görselleştir
- 🌐 **Web Arayüzü** — Bootstrap tabanlı, sade ve kullanımı kolay arayüz

---

## 🧠 Model Mimarisi

Proje iki ayrı derin öğrenme modeli içerir:

### Duygu Modeli (`emotion_model.h5`)
- **Girdi:** 88 tuşlu piyano için 264 boyutlu özellik vektörü (nota sayısı, toplam süre, ortalama velocity)
- **Mimari:** Bidirectional LSTM + Attention Mekanizması + Residual Dense Bloklar
- **Çıktı:** 9 duygu sınıfı için softmax olasılık dağılımı

### Tonalite Modeli (`tonality_model.h5`)
- **Mimari:** Fully Connected Dense katmanları
- **Çıktı:** Major / Minor binary sınıflandırma

### Özellik Çıkarımı
MIDI dosyasındaki her nota için 3 özellik çıkarılır:
1. Nota kullanım sayısı
2. Toplam nota süresi
3. Ortalama velocity (vuruş şiddeti)

Tüm özellikler log normalizasyon + min-max normalizasyon ile ölçeklenir.

---

## 🛠️ Kurulum

**Gereksinim:** Python 3.8+

```bash
# 1. Repoyu klonla
git clone https://github.com/MehmetPekerr/Keysight.git
cd Keysight

# 2. Sanal ortam oluştur ve aktifleştir
python -m venv .venv
.venv\Scripts\activate        # Windows
source .venv/bin/activate     # Linux / macOS

# 3. Bağımlılıkları yükle
pip install -r requirements.txt
```

---

## ▶️ Kullanım

=======
=======
>>>>>>> origin/master
=======
>>>>>>> origin/master
# Müzik Duygu ve Tonalite Analizi

Bu proje, MIDI formatındaki müzik dosyalarını analiz ederek tonaliteyi ve yansıttığı duyguları tespit eden yapay zeka destekli bir web uygulamasıdır.

## Özellikler

- MIDI dosyalarının yüklenmesi ve analizi
- Tonalite tespiti (Major/Minor)
- Duygu analizi ve tahmini
- Görselleştirme ve raporlama
- Kullanıcı dostu web arayüzü

## Kurulum

1. Gerekli Python sürümünü yükleyin (Python 3.8 veya üzeri)

2. Projeyi klonlayın:
```bash
git clone https://github.com/kullaniciadi/muzik-duygu-analizi.git
cd muzik-duygu-analizi
```

3. Sanal ortam oluşturun ve aktifleştirin:
```bash
python -m venv .venv
.venv\Scripts\activate  # Windows için
source .venv/bin/activate  # Linux/Mac için
```

4. Gerekli kütüphaneleri yükleyin:
```bash
pip install -r requirements.txt
```

## Kullanım

1. Web uygulamasını başlatın:
<<<<<<< HEAD
<<<<<<< HEAD
>>>>>>> origin/master
=======
>>>>>>> origin/master
=======
>>>>>>> origin/master
```bash
python app.py
```

<<<<<<< HEAD
<<<<<<< HEAD
<<<<<<< HEAD
Tarayıcıda `http://localhost:5000` adresine git, bir MIDI dosyası yükle ve analiz sonuçlarını görüntüle.

### Analiz Çıktıları
| Çıktı | Açıklama |
|---|---|
| Tonalite | Major veya Minor |
| Tahmin Edilen Duygular | En yüksek olasılıklı 3 duygu |
| Tonalite Duyguları | Tespit edilen tonalitenin çağrıştırdığı duygular |
| Benzerlik Oranı | İki duygu kümesi arasındaki örtüşme yüzdesi |

---

## 📁 Proje Yapısı

```
Keysight/
├── app.py                    # Flask web uygulaması
├── music_emotion_analyzer.py # Model yükleme, özellik çıkarımı ve tahmin
├── note_recognition.py       # MIDI → nota özellik çıkarım ve model eğitim kodu
├── requirements.txt          # Python bağımlılıkları
├── emotion_model.h5          # Eğitilmiş duygu analizi modeli
├── tonality_model.h5         # Eğitilmiş tonalite modeli
├── best_model.h5             # En iyi performanslı model checkpoint
├── note_recognition_model.h5 # Nota tanıma modeli
├── training_results.png      # Eğitim sonuçları görseli
├── maestro-v3.0.0.csv        # MAESTRO veri seti metadata
├── templates/
│   └── index.html            # Web arayüzü (Bootstrap 5 + Chart.js)
└── uploads/                  # Geçici yükleme klasörü (otomatik oluşturulur)
```

---

## 📦 Teknoloji Yığını

| Katman | Teknoloji |
|---|---|
| Web Framework | Flask 2.3 |
| Derin Öğrenme | TensorFlow 2.15 / Keras |
| MIDI İşleme | mido, pretty_midi, music21 |
| Veri İşleme | NumPy, Pandas, scikit-learn |
| Görselleştirme | Matplotlib |
| Frontend | Bootstrap 5, Chart.js |

---

## 📊 Veri Seti

Model eğitimi için [MAESTRO v3.0.0](https://magenta.tensorflow.org/datasets/maestro) (MIDI and Audio Edited for Synchronous TRacks and Organization) veri seti kullanılmıştır. Bu veri seti yaklaşık 200 saatlik piyano performansı içeren profesyonel MIDI kayıtlarından oluşmaktadır.

---

## 🤝 Katkıda Bulunma

1. Bu repoyu fork edin
2. Yeni bir branch oluşturun: `git checkout -b feature/yeni-ozellik`
3. Değişikliklerinizi commit edin: `git commit -m "feat: yeni özellik eklendi"`
4. Branch'inizi push edin: `git push origin feature/yeni-ozellik`
5. Pull Request açın

---

## 📄 Lisans
=======
=======
>>>>>>> origin/master
=======
>>>>>>> origin/master
2. Tarayıcınızda `http://localhost:5000` adresine gidin

3. MIDI dosyası yükleyin ve analiz sonuçlarını görüntüleyin

## Proje Yapısı

```
muzik-duygu-analizi/
├── app.py                    # Web uygulaması
├── music_emotion_analyzer.py # Ana analiz kodu
├── requirements.txt          # Bağımlılıklar
├── emotion_model.h5         # Duygu analizi modeli
├── tonality_model.h5        # Tonalite analizi modeli
├── templates/               # Web arayüzü
│   └── index.html
├── train/                   # Eğitim verileri
├── test/                    # Test verileri
├── val/                     # Doğrulama verileri
└── uploads/                 # Yüklenen dosyalar
```

## Teknolojiler

- Python
- TensorFlow/Keras
- Flask
- pretty_midi
- music21
- matplotlib
- numpy
- pandas

## Analiz Süreci

1. **Nota Analizi**
   - MIDI dosyasından notaların çıkarılması
   - Nota kullanım oranlarının hesaplanması

2. **Tonalite Analizi**
   - Major/Minor tespiti
   - Tonal merkezin belirlenmesi

3. **Duygu Analizi**
   - Duygu tahminleri
   - Benzerlik oranlarının hesaplanması

## Görselleştirme

- Duygu Modeli Sonuçları
- Tonalite Modeli Sonuçları
- Tahmin Edilen Duygular
- Tonalite Dağılımı

## Katkıda Bulunma

1. Bu depoyu fork edin
2. Yeni bir branch oluşturun (`git checkout -b feature/yeniOzellik`)
3. Değişikliklerinizi commit edin (`git commit -am 'Yeni özellik eklendi'`)
4. Branch'inizi push edin (`git push origin feature/yeniOzellik`)
5. Pull Request oluşturun

## Lisans
<<<<<<< HEAD
<<<<<<< HEAD
>>>>>>> origin/master
=======
>>>>>>> origin/master
=======
>>>>>>> origin/master

Bu proje MIT lisansı altında lisanslanmıştır. Detaylar için [LICENSE](LICENSE) dosyasına bakın.
