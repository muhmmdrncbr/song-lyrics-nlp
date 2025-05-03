
# 🎶 Song Lyrics NLP Project

Bu proje, şarkı sözleri üzerinden doğal dil işleme (NLP) teknikleri kullanılarak analiz ve temsil yöntemlerini araştırmaktadır. Amaç, metinsel verilerin temizlenmesi, ön işlenmesi ve makine öğrenmesi modellerine uygun hale getirilerek vektörleştirme yöntemleriyle anlamlı hale getirilmesidir.

---

## 📊 Veri Seti Hakkında

Bu projede kullanılan veri seti, çeşitli müzik türlerinden ve sanatçılardan derlenmiş şarkı sözlerinden oluşmaktadır. Veri seti, şarkı sözlerini temel alarak dil işleme teknikleri ile analiz yapmayı mümkün kılar.

| ✅ Özellik         | 📄 Açıklama                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| 📉 Veri Boyutu      | Yaklaşık 55.000+ şarkı sözü satırı içerir                                 |
| 📂 İçerik           | Her satırda bir şarkı dizesi vardır. Sanatçı/tür bilgisi içerir         |
| 📅 Format           | `.csv` uzantılıdır; metin verisi içerir                                   |
| ✨ Versiyonlama     | `cleaned_lemmatized.csv` ve `cleaned_stemmed.csv` olarak ikiye ayrıldı    |
| 🦜 Ön İşleme        | Noktalama, sayı, özel karakter temizliği + lemmatization & stemming       |
| 🔍 Kullanım Amacı   | Word2Vec, TF-IDF, kelime gömme (embedding) analizlerinde kullanılmıştır   |

> ⚠️ **Not**: Bu veri seti kamuya açık değildir. Akademik çalışma amacıyla sınırlı kullanılmıştır.

---

## 🧠 Proje Amacı

- Şarkı sözleri gibi düzensiz yapılı ve duygusal içerikli metinlerin analiz edilmesi  
- NLP ön işleme teknikleri ile verilerin temizlenmesi  
- TF-IDF ve Word2Vec gibi vektörleştirme yöntemleriyle metnin temsil edilmesi  

---

## 🧰 Kullanılan Kütüphaneler

| 🛋️ Kütüphane       | 🌟 Kullanım Amacı                                                  |
|--------------------|---------------------------------------------------------------------|
| `pandas`           | CSV dosyalarının işlenmesi, veri çerçevesi işlemleri               |
| `numpy`            | Sayısal hesaplamalar, matris/dizi işlemleri                        |
| `re`               | Regex ile metin temizleme                                          |
| `nltk`             | Tokenization, stopword temizliği, lemmatization, stemming          |
| `gensim`           | Word2Vec modeliyle kelime vektörleştirme                           |
| `scikit-learn`     | TF-IDF, eğitim-test bölme, metin vektörleştirme                    |
| `matplotlib`, `seaborn` | Grafiksel görselleştirme ve analiz (opsiyonel)              |

---

## ⚙️ NLP İş Akışı

1. **Veri Temizleme**
   - Küçük harfe dönüştürme
   - Noktalama, sayılar ve özel karakterlerin temizlenmesi
   - Boşluk ve tekrar eden karakterlerin kaldırılması

2. **Stopword Temizliği**
   - `nltk.corpus.stopwords` kullanılarak TR/EN stopword'lerin silinmesi

3. **Lemmatization & Stemming**
   - `WordNetLemmatizer` ve `PorterStemmer` kullanımı

4. **Vektörleştirme**
   - **TF-IDF**: Kelime sıklığına dayalı temsil
   - **Word2Vec**: Anlamsal bağlamı dikkate alan kelime gömme (CBOW/Skip-gram)

---

## 📁 Dosya Yapısı

| 📄 Dosya/Klasör             | 📅 Açıklama                                                                   |
|-----------------------------|-------------------------------------------------------------------------------|
| `nlp_project.ipynb`         | Ana proje dosyası (temizleme, vektörleştirme, modelleme)                     |
| `cleaned_lemmatized.csv`    | Lemmatize edilmiş, temizlenmiş şarkı verileri                                |
| `cleaned_stemmed.csv`       | Stem uygulanmış, temizlenmiş şarkı verileri                                  |
| `.gitignore`                | Büyük dosyaların (model/checkpoint) hariç tutulması için yapılandırma        |
| `README.md`                 | Proje açıklaması, iş akışı, kurulum ve kullanım bilgileri                    |

---

## 📊 Modelleme Notları

- Word2Vec modelleri farklı parametrelerle (`vector size`, `window`, `sg`, `hs`) eğitildi  
- Toplamda **16 farklı Word2Vec modeli** üretildi  
- TF-IDF çıktıları ile karşılaştırmalı analizler yapılabilir hale getirildi  

---

## 🚀 Kurulum ve Kullanım

1. Repoyu klonlayın veya ZIP olarak indirin:
   ```
   https://github.com/muhmmdrncbr/song-lyrics-nlp
   ```

2. Gerekli kütüphaneleri yükleyin (requirements.txt varsa):
   ```
   pip install -r requirements.txt
   ```

3. `nlp_project.ipynb` dosyasını Jupyter Notebook veya VSCode üzerinden çalıştırın.

---

**Hazırlayan:** [@muhmmdrncbr](https://github.com/muhmmdrncbr)  
**Not:** Bu proje yalnızca akademik amaçla geliştirilmiştir.
