# 🕸️ Sosyal Ağ Analizi (SNA): Medya İlişkileri Ağı

Bu proje, medya kuruluşları arasındaki etkileşimleri (bağlantılar, atıflar vb.) **Çizge Teorisi (Graph Theory)** ve **NetworkX** kütüphanesi kullanarak analiz eden bir Python çalışmasıdır.

Proje, ağın topolojik yapısını inceler, en etkili düğümleri (medya kanallarını) belirler ve ağın dayanıklılığını test eder.

## 📋 Proje İçeriği

Bu analiz çalışması aşağıdaki adımları kapsar:

1.  **Veri Hazırlığı:** CSV dosyalarından düğüm (node) ve kenar (edge) verilerinin yüklenmesi ve temizlenmesi.
2.  **Ağ Modellemesi:** Yönlü (Directed) ve Yönsüz (Undirected) grafların oluşturulması.
3.  **Merkeziyet Analizi:**
      * Degree Centrality (Derece)
      * Closeness Centrality (Yakınlık)
      * Betweenness Centrality (Aracılık)
      * Eigenvector & Katz Centrality
      * PageRank Algoritması
4.  **Topluluk Tespiti (Community Detection):** Ağ içindeki modüler yapıların (grupların) belirlenmesi.
5.  **Ağ İstatistikleri:** Yoğunluk (Density), Çap (Diameter), Kümelenme Katsayısı (Clustering Coefficient).
6.  **Görselleştirme:** Ağın topluluklara göre renklendirilmiş grafiği ve derece dağılım histogramları.
7.  **Senaryo Analizi:** En güçlü düğümler ağdan çıkarıldığında yapının nasıl değiştiğinin (Robustness) incelenmesi.

## 🛠️ Gereksinimler

Projeyi çalıştırmak için aşağıdaki Python kütüphanelerine ihtiyacınız vardır:

```bash
pip install pandas numpy matplotlib networkx scipy
```

*Not: Kod, NetworkX 3.0 ve üzeri sürümlerle uyumlu olacak şekilde güncellenmiştir.*

## 📂 Veri Seti Yapısı

Projenin çalışması için çalışma dizininde aşağıdaki iki CSV dosyasının bulunması gerekir:

### 1\. `InputFileNodes.csv` (Düğümler)

Medya kuruluşlarının bilgilerini içerir.

  * **id:** Düğüm kimliği (örn: s01, s02)
  * **media:** Medya adı (örn: NY Times)
  * **media.type:** Medya türü kodu
  * **audience.size:** İzleyici kitlesi büyüklüğü

### 2\. `InputFileEdges.csv` (Kenarlar/İlişkiler)

Kuruluşlar arasındaki bağlantıları içerir.

  * **from:** Kaynak düğüm ID
  * **to:** Hedef düğüm ID
  * **weight:** İlişkinin ağırlığı
  * **type:** İlişki türü (hyperlink, mention vb.)

## 🚀 Kurulum ve Kullanım

1.  Bu repoyu klonlayın veya dosyaları indirin.
2.  Jupyter Notebook veya Google Colab ortamında `kaaödev.ipynb` dosyasını açın.
3.  CSV dosyalarının notebook ile aynı klasörde olduğundan emin olun.
4.  Hücreleri sırasıyla çalıştırın.

## 📊 Örnek Çıktılar

Analiz sonucunda elde edilen bazı önemli metrikler şunlardır:

  * **En Kritik Köprü Düğüm (Betweenness):** Farklı gruplar arasındaki bilgi akışını sağlayan ana medya organı.
  * **En Popüler Düğüm (Degree):** En çok bağlantıya sahip olan medya.
  * **Modülarite (Modularity):** Ağın ne kadar belirgin gruplara ayrıldığının göstergesi (0.3 üstü genelde güçlü bir topluluk yapısını işaret eder).
  * **Küçük Dünya (Small World):** Düğümler arası ortalama yol uzunluğunun kısalığı.

## 📈 Görselleştirme

Proje, ağın yapısını anlamak için **Matplotlib** kullanarak detaylı görseller üretir:

  * Düğüm büyüklükleri **dereceye (degree)** göre ayarlanmıştır.
  * Düğüm renkleri ait oldukları **topluluklara (communities)** göre belirlenmiştir.

## 🤝 Katkıda Bulunma

Hatalı bir analiz veya geliştirme öneriniz varsa lütfen "Pull Request" gönderin veya "Issue" açın.

## 📝 Lisans

Bu proje eğitim amaçlı hazırlanmıştır. Açık kaynak olarak kullanılabilir.

-----

**Hazırlayan:** [Muhammed KÖSE]
