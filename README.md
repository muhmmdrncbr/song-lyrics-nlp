# 🎶 Song Lyrics NLP Project

Bu proje, şarkı sözleri üzerinden doğal dil işleme (NLP) teknikleri kullanılarak analiz ve temsil yöntemlerini araştırmaktadır. Amaç, metinsel verilerin temizlenmesi, ön işlenmesi ve makine öğrenmesi modellerine uygun hale getirilerek vektörleştirme yöntemleriyle anlamlı temsil edilmesidir.

## 🧠 Proje Amacı

 Şarkı sözleri gibi yapısı düzensiz ve duygusal yüklü metinlerin işlenmesi
-NLP teknikleri ile temizleme, önişleme, gömme (embedding) yöntemlerinin uygulanması
-Gömülü kelime temsilleri (TF-IDF & Word2Vec) üretip modellemeye hazır hale getirmek

## 🧰 Kullanılan Kütüphaneler

| Kütüphane | Kullanım Amacı |
| `pandas` | Veri okuma ve CSV dosyaları ile çalışma |
| `numpy` | Sayısal işlemler ve matris hesaplamaları |
| `re` | Regex ile metin temizleme işlemleri |
| `nltk` | Tokenizasyon, stopword temizliği, lemmatization, stemming |
| `gensim` | Word2Vec modeli ile kelime gömme (embedding) işlemleri |
| `sklearn` | TF-IDF vektörleştirme, veri bölme ve diğer preprocessing işlemleri |
| `matplotlib`, `seaborn` *(isteğe bağlı)* | Görselleştirme ve analiz grafikleri oluşturma |

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

| Dosya | Açıklama |
| `nlp_project.ipynb` | Ana proje not defteri. Tüm işlemler buradan yürütülmektedir. |
| `cleaned_lemmatized.csv` | Temizlenmiş ve lemmatize edilmiş şarkı sözleri |
| `cleaned_stemmed.csv` | Temizlenmiş ve stem uygulanmış şarkı sözleri |
| `.gitignore` | Büyük boyutlu dosyaların (model, checkpoint) dışlanması için kullanılır |
| `README.md` | Proje tanıtımı, açıklamalar ve kullanım kılavuzu |

> ⚠️ Not: `.model` dosyaları (Word2Vec çıktıları) ve `.ipynb_checkpoints/` klasörü `.gitignore` ile hariç tutulmuştur. Modelin nasıl üretildiği kod ile gösterilmiştir.



## 📊 Modelleme Notları

-**Word2Vec** modelleri farklı parametrelerle (`window`, `size`, `sg`, `hs`) eğitildi.
-Eğitim sonucunda toplamda 16 farklı model oluşturuldu.
-TF-IDF çıktıları ile karşılaştırmalı analiz yapılabilir hale getirildi.

## 🚀 Kurulum ve Kullanım

1. Projeyi klonlayın veya indirin:
https://github.com/muhmmdrncbr/song-lyrics-nlp
