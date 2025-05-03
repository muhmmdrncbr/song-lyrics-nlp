🎶 Song Lyrics NLP Project

Bu proje, şarkı sözleri üzerinden doğal dil işleme (NLP) teknikleri kullanılarak analiz ve temsil yöntemlerini araştırmaktadır. Amaç, metinsel verilerin temizlenmesi, ön işlenmesi ve makine öğrenmesi modellerine uygun hale getirilerek vektörleştirme yöntemleriyle anlamlı temsil edilmesidir.

📊 Veri Seti Hakkında

Bu projede kullanılan veri seti, çeşitli müzik türlerinden ve sanatçılardan derlenmiş şarkı sözlerinden oluşmaktadır. Veri seti, şarkı sözlerini temel alarak dil işleme teknikleri ile analiz yapmayı mümkün kılar.



✅ Özellik                     📄 Açıklama

📉 Veri Boyutu                 Toplamda yaklaşık 10.000+ şarkı sözü satırı içerir.

📂 İçerik                      Her satırda bir şarkı dizesi vardır.Sanatçı/tür bilgisi yer almaz.

📅 Format                      .csv uzantılı, metin verisi içerir.

✨ Versiyonlama                cleaned_lemmatized.csv ve cleaned_stemmed.csv olarak iki farklı versiyona ayrıldı.

🦜 Ön İşleme                   Noktalama, sayılar, özel karakterler temizlenip; lemmatization ve stemming uygulandı.

🔍 Kullanım Amaçları            Word2Vec, TF-IDF, embedding analizleri için kullanıldı.




⚠️ Not: Bu veri seti kamuya açık değildir. Akademik çalışma amacıyla sınırlı kullanılmıştır.



🧠 Proje Amacı

*Şarkı sözleri gibi düzensiz yapılı ve duygusal içerikli metinlerin işlenmesi

*NLP ön işleme teknikleri ile temizleme ve düzenleme

*TF-IDF ve Word2Vec gibi vektörleştirme yöntemleriyle metni temsil edilebilir hale getirme


🧰️ Kullanılan Kütüphaneler

🛋️ Kütüphane                 🌟 Kullanım Amacı

pandas                        Veri çerçevesi oluşturma, CSV işlemleri

numpy                         Dizi, matris ve sayısal hesaplamalar

re                            Regular Expression (regex) ile metin temizleme

nltk                          Tokenizasyon, stopword temizliği, lemmatizasyon, stemming

gensim                        Word2Vec modeli ile kelime vektörleri oluşturma

scikit-learn                  TF-IDF vektörleştirme, veri bölme, ön işleme

matplotlib, seaborn           Grafik çizimi ve görselleştirme (isteğe bağlı)



⚙️ Uygulanan NLP İŞ Akışı

1)Veri Temizleme:

*Küçük harfe çevirme

*Sayı, noktalama ve özel karakterlerin silinmesi

*Boşluk ve tekrar eden karakter temizliği

2)Stopword Temizliği:

*nltk.corpus.stopwords ile anlamsız kelimelerin silinmesi (TR/EN)

3)Lemmatization & Stemming:

*WordNetLemmatizer ve PorterStemmer kullanıldı

4)Vektörleştirme:

*TF-IDF: Kelime frekansına dayalı temsiller

*Word2Vec: Anlamsal bağlam temelli kelime vektörleri (CBOW/Skip-gram)



📁 Dosya Yapısı

📄 Dosya/Klasör                📅 Açıklama

nlp_project.ipynb              Ana Proje(temizleme, vektörleştirme, modelleme)

cleaned_lemmatized.csv         Lemmatize edilmiş, temizlenmiş şarkı verileri
 
cleaned_stemmed.csv            Stem uygulanmış, temizlenmiş şarkı verileri

.gitignore                     Model/ara çıktılar gibi büyük dosyaları ignore etmek için

README.md                      Proje tanıtımı, kurulum, iş akışı ve açıklamalar



📊 Modelleme Notları

*Word2Vec modelleri farklı parametrelerle (vector size, window, sg, hs) eğitildi.

*Toplamda 16 farklı Word2Vec modeli eğitildi.

*TF-IDF çıktıları ile kıyaslama ve görsel analizler yapılabilir.

🚀 Kurulum ve Kullanım

1)Repoyu klonlayın veya ZIP olarak indirin:

https://github.com/muhmmdrncbr/song-lyrics-nlp

2)Ortamınızda gerekli kütüphaneleri yükleyin:

pip install -r requirements.txt  # (varsa)

3)nlp_project.ipynb dosyasını açın ve adım adım çalıştırın.

Hazırlayan: @muhmmdrncbr

Proje sadece akademik amaçlarla geliştirilmiştir.