# 🎶 Song Lyrics NLP Project

Bu proje, şarkı sözleri üzerinden doğal dil işleme (NLP) teknikleri kullanılarak analiz ve temsil yöntemlerini araştırmaktadır. Amaç, metinsel verilerin temizlenmesi, ön işlenmesi ve makine öğrenmesi modellerine uygun hale getirilerek vektörleştirme yöntemleriyle anlamlı temsil edilmesidir.

📊 Veri Seti Hakkında

Bu projede kullanılan veri seti, çeşitli müzik türlerinden ve sanatçılardan derlenmiş şarkı sözlerinden oluşmaktadır. Veri seti, şarkı sözlerini temel alarak dil işleme teknikleri ile analiz yapmayı mümkün kılar.
Özellik	Açıklama
🔢 Veri Boyutu	Toplamda X adet şarkı sözü satırı içerir (örneğin: 10.000 satır).
🗂️ İçerik	Her satırda bir şarkı söz dizesi bulunur. Tür, sanatçı veya albüm bilgisi yer almaz.
📄 Format	Veri .csv formatındadır ve analiz öncesi cleaned_lemmatized.csv ve cleaned_stemmed.csv olarak iki farklı versiyona ayrılmıştır.
🧹 Ön İşleme	Verilerden noktalama işaretleri, özel karakterler ve sayılar temizlenmiş; ardından lemmatizasyon ve stemming uygulanmıştır.
📌 Amaç	Bu veri seti, kelime temsillerinin oluşturulması, TF-IDF analizi, Word2Vec gömme ve benzeri NLP işlemlerinde kullanılmıştır.

Not: Bu veri seti kamuya açık değildir. Projede eğitim ve akademik amaçlarla sınırlı şekilde kullanılmıştır.

## 🧠 Proje Amacı

 Şarkı sözleri gibi yapısı düzensiz ve duygusal yüklü metinlerin işlenmesi
-NLP teknikleri ile temizleme, önişleme, gömme (embedding) yöntemlerinin uygulanması
-Gömülü kelime temsilleri (TF-IDF & Word2Vec) üretip modellemeye hazır hale getirmek

🧰 Kullanılan Kütüphaneler

📦 Kütüphane	🎯 Kullanım Amacı
pandas	CSV dosyalarının okunması, veri çerçeveleri ile çalışma, veri manipülasyonu
numpy	Sayısal hesaplamalar, dizi/matris işlemleri
re	Regular expression kullanarak metin temizleme ve desen eşleştirme
nltk	Doğal dil işleme: tokenization, stopword temizliği, lemmatization ve stemming
gensim	Word2Vec gibi gömme (embedding) algoritmalarını kullanarak kelime vektörleri üretme
scikit-learn	TF-IDF vektörleştirme, eğitim-test bölme, ön işleme ve temel makine öğrenmesi araçları
matplotlib, seaborn (opsiyonel)	Grafiksel veri görselleştirme ve analiz amacıyla kullanılmıştır


## ⚙️ Uygulanan NLP İş Akışı



1. **Veri Temizleme (Preprocessing)**
   -Küçük harfe çevirme
   -Sayılar ve noktalama işaretlerinin silinmesi
   -Gereksiz boşlukların ve karakterlerin temizlenmesi

2. **Stopword Temizliği**
    Türkçe ve İngilizce stopword listeleri ile anlam taşımayan kelimeler çıkarıldı.

3. **Lemmatization & Stemming**
   -`nltk.WordNetLemmatizer` ve `PorterStemmer` ile kelimelerin kök halleri elde edildi.

4. **Vektörleştirme (Text Embedding)**
    **TF-IDF**: Kelime frekanslarına dayalı vektör temsil
    **Word2Vec**: Kelime ilişkilerini öğrenen gömme modeli (CBOW/Skip-gram)

## 📁 Dosya Yapısı

📄 Dosya / Klasör	📌 Açıklama
nlp_project.ipynb	Ana proje not defteri. Veri temizleme, vektörleştirme ve modelleme işlemleri bu dosyada gerçekleştirilmiştir.
cleaned_lemmatized.csv	Temizlenmiş ve lemmatize edilmiş şarkı sözlerini içerir.
cleaned_stemmed.csv	Temizlenmiş ve köklerine indirgenmiş (stemmed) şarkı sözlerini içerir.
.gitignore	Büyük boyutlu dosyaların (model, checkpoint gibi) repodan hariç tutulması için yapılandırma dosyasıdır.
README.md	Proje açıklaması, kullanılan yöntemler ve çalıştırma talimatlarını içeren dökümantasyon dosyasıdır.




## 📊 Modelleme Notları

-**Word2Vec** modelleri farklı parametrelerle (`window`, `size`, `sg`, `hs`) eğitildi.
-Eğitim sonucunda toplamda 16 farklı model oluşturuldu.
-TF-IDF çıktıları ile karşılaştırmalı analiz yapılabilir hale getirildi.

## 🚀 Kurulum ve Kullanım

1. Projeyi klonlayın veya indirin:
https://github.com/muhmmdrncbr/song-lyrics-nlp
