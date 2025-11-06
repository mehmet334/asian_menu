
# 🍜 Asian Kitchen's Menu

Bu proje, **JavaScript ile dinamik menü oluşturma** konusunu pekiştirmek için hazırlanmıştır.
HTML ve CSS dosyaları hazır olarak verilmiş, öğrencilerden **JavaScript kısmını** tamamlamaları beklenmiştir.

---

## 🎯 Amaç

Kullanıcıların **kategori butonları** (örneğin *Korea*, *Japan*, *China*) üzerinden filtreleme yaparak menüdeki yemekleri dinamik şekilde görüntülemesini sağlamak.
HTML sabit, JavaScript ise içeriği veri dizisinden üretir.

---

## 🧠 Kazanımlar

Bu projeyle birlikte aşağıdaki konular pekiştirilecektir:

* **Array metodları**: `map()`, `filter()`, `reduce()`
* **DOM manipülasyonu**: `innerHTML`, `querySelector`, `addEventListener`
* **Diziden HTML oluşturma**
* **Kategori bazlı filtreleme**
* **Dynamic Button Rendering (JS ile buton üretme)**

---

## 🗂️ Klasör Yapısı

```
Asian-Kitchen-Menu/
│
├── index.html         # Temel yapı (size hazır verildi)
├── style.css          # Tasarım dosyası (size hazır verildi)
└── app.js             # JavaScript kodları (sizin tamamlayacağınız kısım)
```

---

## 🍱 JavaScript İçeriği

Menü içeriği `app.js` dosyasında bir dizi olarak tanımlanacaktır:

```js
const menu = [
  {
    id: 1,
    title: "Tteokbokki",
    category: "Korea",
    price: 10.99,
    img: "./images/item-1.jpeg",
    desc: "Spicy rice cakes, serving with fish cake."
  },
  {
    id: 2,
    title: "Chicken Ramen",
    category: "Japan",
    price: 7.99,
    img: "./images/item-2.jpeg",
    desc: "Chicken noodle soup, with vegetables."
  },
  // ... devamı
];
```

### 🔹 Butonlar da JS ile oluşturulacak

```js
const categories = ["All", ...new Set(menu.map(item => item.category))];
```

### 🔹 Filtreleme mantığı

```js
function filterMenu(category) {
  const filtered = category === "All" ? menu : menu.filter(item => item.category === category);
  displayMenu(filtered);
}
```

---

## 💻 Kullanım

1. Projeyi bilgisayarına indir:

   ```bash
   git clone https://github.com/kullaniciadi/asian-kitchen-menu.git
   cd asian-kitchen-menu
   ```

2. Dosyaları bir editörle aç (ör. VS Code).

3. `app.js` dosyasındaki menü ve filtreleme kodlarını tamamla.

4. `index.html` dosyasını çift tıklayarak tarayıcıda aç.

---

## 📸 Örnek Ekran

```
-----------------------------------------
| Asian Kitchen's Menu                  |
| [All] [Korea] [Japan] [China]         |
-----------------------------------------
| 🥢 Tteokbokki - 10.99 ₺               |
| Spicy rice cakes, serving with fish.  |
-----------------------------------------
| 🍜 Chicken Ramen - 7.99 ₺             |
| Chicken noodle soup, with vegetables. |
-----------------------------------------
```

---

## 🔧 Önerilen Geliştirmeler

* Arama çubuğu ekleme (`input` + `keyup` ile)
* Fiyat sıralama (`sort` kullanarak)
* Görsel hover animasyonu
* Menü verilerini dış JSON dosyasından çekme

---
