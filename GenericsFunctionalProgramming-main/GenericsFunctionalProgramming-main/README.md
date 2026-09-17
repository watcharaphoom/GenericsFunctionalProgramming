# Lab : Generics & Functional Programming (Stream API)

วิชา 01418211 Software Construction

## ส่วนที่ 0: ไฟล์เริ่มต้น

นิสิตจะได้รับโปรเจกต์ที่มี 3 ไฟล์

| ไฟล์ | หน้าที่ |
|---|---|
| `Product.java` | `record Product(id, name, category, price, stock)` |
| `ProductAnalytics.java` | คลาสวิเคราะห์สินค้า (เขียนด้วย for loop) |
| `ProductAnalyticsTest.java` | เทสต์ที่สมบูรณ์อยู่แล้ว ใช้ตรวจสอบ `ProductAnalytics` |

---

## ส่วนที่ 1: สร้าง Generic Class

1. สร้างไฟล์ใหม่ `Pair.java`
2. สร้าง Generic Class ชื่อ `Pair<K, V>` ที่สามารถเก็บอ็อบเจกต์ได้ 2 ชนิด (Key และ Value)
   - **Rep:** มีฟิลด์ `private final K key;` และ `private final V value;`
   - **Constructor:** รับ `key` และ `value`
   - **Getters:** สร้างเมธอด `getKey()` และ `getValue()`
3. **สร้างไฟล์ทดสอบ:** สร้างคลาส `PairTest` ที่มีเมธอด `main` เพื่อทดลองสร้าง
   - `Pair<String, Integer>`
   - `Pair<Product, Boolean>`

   เพื่อพิสูจน์ว่าคลาสของคุณทำงานได้กับทุกชนิดข้อมูล

---

## ส่วนที่ 2: Refactoring to Functional Style (75 นาที)

1. เปิดไฟล์ `ProductAnalytics.java`
2. Refactor เมธอดทั้ง 4 ในคลาสให้เปลี่ยนมาใช้ **Stream API** แทน for loop
   - `findProductsByCategory`
   - `getProductNamesWithPriceLessThan`
   - `calculateTotalStockValueForCategory`
   - `hasProductOutOfStock`
3. **รันเทสต์:** รันไฟล์ `ProductAnalyticsTest.java` เพื่อตรวจสอบว่าโค้ดใหม่ของคุณยังคงทำงานได้ถูกต้อง


