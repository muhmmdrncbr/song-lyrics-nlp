# song-lyrics-nlp
Song lyrics NLP project

# 🎵 Song Lyrics NLP – Şarkı Sözlerinden Öneri Sistemi

Bu proje, şarkı sözlerinden yola çıkarak içerik tabanlı bir öneri sistemi geliştirmeyi amaçlar.  
TF-IDF ve Word2Vec gibi vektörleştirme yöntemleri ile şarkıların anlamsal yakınlıkları çıkarılır ve benzer şarkılar önerilir.


## 📂 Veri Seti

- **Kaynak**: Kaggle  
- **Veri adı**: `spotify_millsongdata.csv`  
- **İçerik**: 55.000'den fazla şarkı sözü, sanatçı adı ve bağlantı içerir  
- **Amaç**: Şarkıların sözlerine göre öneri yapmak

Örnek sütunlar:  
- `artist`: Şarkıcı adı  
- `song`: Şarkı adı  
- `text`: Şarkı sözleri


## 🔧 Uygulanan Adımlar

1. **Veri Yükleme** – Kaggle’dan alınan CSV veri seti okundu  
2. **Ön İşleme** – Temizlik, küçük harf, noktalama, stopword, lemmatization, stemming  
3. **Zipf Analizi** – Ham ve temizlenmiş verilerde dağılım grafikleri oluşturuldu  
4. **Vektörleştirme**  
   - TF-IDF: Belge temsili (1000 kelimeye indirgenmiş)  
   - Word2Vec: 8 farklı parametre kombinasyonu ile model eğitildi  
5. **Öneri Sistemleri**  
   - TF-IDF + cosine similarity  
   - Word2Vec + vektör ortalaması + cosine similarity  
6. **Benzerlik Testi ve Görselleştirme**  
   - PCA ile 2D gösterim  
   - Bar plot ile en benzer kelimeler  
7. **Kıyaslama ve Sonuç**  
   - TF-IDF vs Word2Vec karşılaştırıldı  



## ⚙️ Gerekli Kütüphaneler ve Kurulum

Projeyi çalıştırmadan önce aşağıdaki Python kütüphanelerinin kurulu olması gerekir:

pip install pandas numpy matplotlib scikit-learn gensim nltk 

Ayrıca nltk veri kaynakları (stopwords, punkt, wordnet) indirilmelidir:

import nltk
nltk.download("punkt")
nltk.download("stopwords")
nltk.download("wordnet")


## 📈 Sonuç ve Değerlendirme

Bu projede şarkı sözlerinden yola çıkarak içerik tabanlı bir öneri sistemi geliştirilmiştir.  
TF-IDF ve Word2Vec yöntemleri ile öneriler yapılmış, benzerlik skorları görselleştirilmiş ve semantik benzerlik test edilmiştir.

- **TF-IDF** daha yüzeysel benzerlikleri yakalarken,
- **Word2Vec**, anlam bütünlüğünü daha iyi yakalayarak daha doğal öneriler üretmiştir.

Gelecekte, bu sisteme kullanıcı verileri de entegre edilerek daha güçlü, **hibrit bir öneri sistemi** oluşturulabilir.

