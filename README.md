# 🛒 Olist E-Commerce Data Analysis (Python)

Bu proje, Brezilya'nın en büyük e-ticaret platformlarından biri olan **Olist** veri seti kullanılarak hazırlanmış kapsamlı bir Python veri analizi çalışmasıdır.  
Amaç; sipariş davranışlarını, fiyat dağılımlarını, teslimat sürelerini, müşteri memnuniyetini ve ödeme yöntemlerinin tamamlanma oranlarını analiz etmektir.

---

## 🛠️ Tools & Technologies
- **Python (Google Colab)**
- **Pandas · NumPy**
- **Plotly Express**
- **Matplotlib · Seaborn**
- **SciPy (Chi-Square Test)**
- **EDA + Feature Engineering**

---

## 📥 1. Data Loading & Preparation

Projede kullanılan veri setleri:

- `olist_orders_dataset.csv`  
- `olist_order_items_dataset.csv`  
- `olist_products_dataset.csv`  
- `olist_customers_dataset.csv`  
- `olist_sellers_dataset.csv`  
- `olist_order_payments_dataset.csv`  
- `olist_order_reviews_dataset.csv`

Notebook’ta ilk olarak tüm CSV dosyaları **pandas DataFrame** olarak yüklendi, gerekli kolon seçimi ve temizliği yapıldı.

---

## 🔍 2. Exploratory Data Analysis (EDA)

Analiz kapsamında yapılan temel incelemeler:

### ✔️ Sipariş fiyatı istatistikleri  
- Ortalama ürün fiyatı  
- Order bazında toplam sepet tutarı  
- En yüksek ve en düşük fiyatlı ürünler  
- Kategori bazında fiyat karşılaştırmaları  

### ✔️ Ürün kategorisi analizleri  
- En çok sipariş edilen kategoriler  
- En yüksek gelir getiren kategoriler  
- “Informática Acessórios” gibi kategorilerin fiyat davranışları

### ✔️ Teslimat süresi analizi  
- `order_purchase_timestamp` → `order_delivered_customer_date` farkı  
- Ortalama teslim süresi  
- Geciken teslimatların oranı  
- Gecikmenin yorum puanlarına etkisi

---

## 📊 3. Visualizations

Notebook’ta aşağıdaki grafikler oluşturulmuştur:

- Toplam sepet tutarı dağılımı  
- Kategori bazında ortalama fiyat grafiği  
- Teslim süreleri dağılım grafiği  
- Ürün kategorisi popülerliği  
- İnceleme puanı dağılımı  
- Ödeme yöntemi tamamlanma oranları çubuğu  

Tüm grafikler **Plotly Express** veya **Matplotlib** ile oluşturulmuştur.

---

## 📈 4. Statistical Test — Chi-Square Hypothesis Test

Analiz edilen hipotez:

### **H0:** Ödeme yöntemi, siparişin tamamlanma oranını etkilemez  
### **H1:** Ödeme yöntemi, tamamlanma oranını etkiler

Notebook’ta:

- Ödeme yöntemi × sipariş tamamlanma durumu için **contingency table** oluşturuldu  
- SciPy ile **chi-square** testi uygulandı  
- Sonuç → *p < 0.05* bulundu

➡️ **Ödeme yönteminin siparişin iptal edilip edilmemesi üzerinde anlamlı etkisi vardır.**

Kredi kartı en güvenilir yöntemdir; alternatif yöntemlerde iptal oranları daha yüksektir.

---

## 💡 5. Key Insights

- ⚠️ Teslim süresi uzadıkça **review score düşüyor**  
- 💳 Kredi kartı siparişleri en yüksek tamamlanma oranına sahip  
- ⏳ Geciken teslimatlar memnuniyeti ciddi şekilde etkiliyor  
- 💸 Bazı kategoriler (ör. “Informática Acessórios”) daha yüksek fiyat ortalamasına sahip  
- 📦 En yoğun kategori grupları en yüksek gelirleri getiriyor

---

## 🧠 6. Business Recommendations

- Lojistik zinciri iyileştirilerek gecikme oranları azaltılmalı  
- Yüksek değerli kategorilere stok & kampanya yatırımı yapılmalı  
- Ödeme yöntemi seçim ekranlarında kredi kartı önerisi yapılabilir  
- Gecikme riskinin yüksek olduğu bölgeler için ayrı SLA tanımlanabilir  
- Müşteri deneyimi yönetimi için review score analizi düzenli yapılmalı

---

## 👩‍💻 Author

**Gökçe Tür – Data Analyst**  
Python · Power BI · SQL · BigQuery · Looker Studio  
GitHub: **gokceturr**


