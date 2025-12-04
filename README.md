İsteğin üzerine README.md dosyasını, MIT Lisansı'nı ve senin adını içerecek şekilde güncelledim. Aşağıdaki metni kopyalayıp kullanabilirsin.

🕸️ Sosyal Ağ Analizi (SNA): Medya İlişkileri Ağı
Bu proje, medya kuruluşları arasındaki etkileşimleri (bağlantılar, atıflar vb.) Çizge Teorisi (Graph Theory) ve NetworkX kütüphanesi kullanarak analiz eden bir Python çalışmasıdır.

Proje, ağın topolojik yapısını inceler, en etkili düğümleri (medya kanallarını) belirler ve ağın dayanıklılığını test eder.

📋 Proje İçeriği
Bu analiz çalışması aşağıdaki adımları kapsar:

Veri Hazırlığı: CSV dosyalarından düğüm (node) ve kenar (edge) verilerinin yüklenmesi ve temizlenmesi.

Ağ Modellemesi: Yönlü (Directed) ve Yönsüz (Undirected) grafların oluşturulması.

Merkeziyet Analizi:

Degree Centrality (Derece)

Closeness Centrality (Yakınlık)

Betweenness Centrality (Aracılık)

Eigenvector & Katz Centrality

PageRank Algoritması

Topluluk Tespiti (Community Detection): Ağ içindeki modüler yapıların (grupların) belirlenmesi.

Ağ İstatistikleri: Yoğunluk (Density), Çap (Diameter), Kümelenme Katsayısı (Clustering Coefficient).

Görselleştirme: Ağın topluluklara göre renklendirilmiş grafiği ve derece dağılım histogramları.

Senaryo Analizi: En güçlü düğümler ağdan çıkarıldığında yapının nasıl değiştiğinin (Robustness) incelenmesi.

🛠️ Gereksinimler
Projeyi çalıştırmak için aşağıdaki Python kütüphanelerine ihtiyacınız vardır:

Bash

pip install pandas numpy matplotlib networkx scipy
Not: Kod, NetworkX 3.0 ve üzeri sürümlerle uyumlu olacak şekilde güncellenmiştir.

📂 Veri Seti Yapısı
Projenin çalışması için çalışma dizininde aşağıdaki iki CSV dosyasının bulunması gerekir:

1. InputFileNodes.csv (Düğümler)
Medya kuruluşlarının bilgilerini içerir.

id: Düğüm kimliği (örn: s01, s02)

media: Medya adı (örn: NY Times)

media.type: Medya türü kodu

audience.size: İzleyici kitlesi büyüklüğü

2. InputFileEdges.csv (Kenarlar/İlişkiler)
Kuruluşlar arasındaki bağlantıları içerir.

from: Kaynak düğüm ID

to: Hedef düğüm ID

weight: İlişkinin ağırlığı

type: İlişki türü (hyperlink, mention vb.)

🚀 Kurulum ve Kullanım
Bu repoyu klonlayın veya dosyaları indirin.

Jupyter Notebook veya Google Colab ortamında kaaödev.ipynb dosyasını açın.

CSV dosyalarının notebook ile aynı klasörde olduğundan emin olun.

Hücreleri sırasıyla çalıştırın.

📊 Örnek Çıktılar
Analiz sonucunda elde edilen bazı önemli metrikler şunlardır:

En Kritik Köprü Düğüm (Betweenness): Farklı gruplar arasındaki bilgi akışını sağlayan ana medya organı.

En Popüler Düğüm (Degree): En çok bağlantıya sahip olan medya.

Modülarite (Modularity): Ağın ne kadar belirgin gruplara ayrıldığının göstergesi (0.3 üstü genelde güçlü bir topluluk yapısını işaret eder).

Küçük Dünya (Small World): Düğümler arası ortalama yol uzunluğunun kısalığı.

📈 Görselleştirme
Proje, ağın yapısını anlamak için Matplotlib kullanarak detaylı görseller üretir:

Düğüm büyüklükleri dereceye (degree) göre ayarlanmıştır.

Düğüm renkleri ait oldukları topluluklara (communities) göre belirlenmiştir.

🤝 Katkıda Bulunma
Hatalı bir analiz veya geliştirme öneriniz varsa lütfen "Pull Request" gönderin veya "Issue" açın.

📝 Lisans
Bu proje MIT Lisansı ile lisanslanmıştır.

MIT License

Copyright (c) 2025 Muhammed KÖSE

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Hazırlayan: Muhammed KÖSE
