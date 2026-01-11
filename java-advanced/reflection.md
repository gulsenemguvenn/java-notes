# Reflection

## **📌 Reflection Nedir ve Nasıl Çalışır?**

Reflection, çalışma zamanında programın yapısını incelemenize ve dinamik olarak değiştirebilmenize olanak tanır. `java.lang.reflect` paketinde yer alan sınıflarla gerçekleştirilir. Reflection, genellikle framework'lerde ve kütüphanelerde, esnek yapıların oluşturulması amacıyla kullanılır. Örneğin, Spring ve Hibernate gibi popüler Java framework'leri reflection kullanarak sınıfları analiz eder ve dinamik işlemler yapar.

---

## **📌 Reflection Kullanımı**

### **1. Class Sınıfı**

Java'da bir sınıfı yansıtmada kullanılan temel sınıf `Class`’tır. `Class` sınıfı, sınıflarla ilgili metadata'yı (sınıf adı, metodlar, alanlar vb.) tutar ve aynı zamanda nesnelerin sınıf türünü almak için de kullanılır.

📌 Örnek:

![alt text](image-92.png)

✅ **Önemli Nokta:** `Class.forName("ClassName")` ile sınıfın `Class` nesnesine erişebilirsiniz. Bu, sınıfın tam adını vererek gerçekleştirilir.

---

### **2. Field (Alan) Erişimi**

Bir sınıfın alanlarını yansıtmak için `getDeclaredFields()` metodu kullanılır. Bu metot, o sınıftaki tüm alanları döndürür.

📌 Örnek:

![alt text](image-93.png)

✅ **Önemli Nokta:** `setAccessible(true)` ile private alanlara erişilebilirlik sağlanabilir.

---

### **3. Method Erişimi**

Bir sınıfın metodlarını yansıtmak için `getDeclaredMethods()` veya `getMethods()` kullanılır. Bu metotlar, sınıfın veya onun miras aldığı sınıfların metodlarını döndüren Reflection metotlarıdır.

📌 Örnek:

![alt text](image-94.png)

✅ **Önemli Nokta:** `invoke()` metodu, yansıtılan metodu çağırmak için kullanılır. Parametre gerektiren bir metod ise uygun parametrelerle çağrılmalıdır.

---

### **4. Constructor Erişimi**

Constructorları yansıtmak için `getDeclaredConstructor()` metodu kullanılır. Bu metot, belirli bir constructor'ı almak için kullanılabilir.

📌 Örnek:

![alt text](image-95.png)

✅ **Önemli Nokta:** `newInstance()` metodu ile constructor çağrılabilir. `setAccessible(true)` ile private constructor'lara erişilebilirlik sağlanabilir.

---

## **📌 Reflection'ın Kullanım Alanları**

- **Dynamic Proxy:** Reflection, proxy sınıflarının oluşturulmasında kullanılabilir.
- **Framework ve Kütüphaneler:** Spring, Hibernate gibi framework'ler sınıf türlerini dinamik olarak keşfetmek ve işlem yapmak için reflection kullanır.
- **Dependency Injection (DI):** Nesnelerin çalışma zamanında enjekte edilmesinde reflection kullanılır.

---

## **📌 Reflection'ın Dezavantajları**

- **Performans Sorunları:** Reflection, doğrudan kod yazımına göre daha yavaştır çünkü çalışma zamanında sınıf bilgilerine erişir.
- **Güvenlik Sorunları:** Private ve protected üyelere erişim sağlanması, güvenlik risklerine yol açabilir.
- **Karmaşıklık:** Reflection kullanımı kodunuzu karmaşıklaştırabilir ve bakımını zorlaştırabilir.

---

## **📌 Mülakat Soruları ve Cevapları**

### **1️⃣ Reflection nedir ve ne amaçla kullanılır?**
**Cevap:** Reflection, Java'da çalışma zamanında bir sınıfın metadatasına (sınıf adı, metodlar, alanlar) erişmek için kullanılan bir tekniktir. Ayrıca çalışma zamanında sınıfları, metodları ve constructor'ları dinamik olarak keşfetmek ve kullanmak için de kullanılır. Genellikle framework ve kütüphanelerde dinamik nesne oluşturma ve işlem yapma amaçlı kullanılır.

---

### **2️⃣ Reflection API'yi kullanarak bir nesnenin metotlarına nasıl erişilir?**
**Cevap:** Reflection API ile bir nesnenin metodlarına erişmek için `getDeclaredMethods()` veya `getMethods()` metodları kullanılır. Daha sonra, `Method` nesnesinin `invoke()` metodu ile bu metotları çalıştırabilirsiniz.

---

### **3️⃣ Reflection ile private alanlara erişilebilir mi?**
**Cevap:** Evet, Reflection ile private alanlara erişilebilir. Ancak bunun için `setAccessible(true)` metodu kullanılarak alanın erişilebilir olması sağlanmalıdır.

---

### **4️⃣ Reflection kullanmanın dezavantajları nelerdir?**
**Cevap:**
- **Performans Sorunları:** Reflection, doğrudan erişime kıyasla daha yavaştır çünkü çalışma zamanında sınıf bilgilerine erişim sağlanır.
- **Güvenlik Sorunları:** Private ve protected üyelerin erişimi, güvenlik açıklarına yol açabilir.
- **Karmaşıklık:** Reflection kullanımı kodunuzu daha karmaşık ve bakımı zor hale getirebilir.

---

### **5️⃣ Reflection API ile bir constructor'a nasıl erişilir?**
**Cevap:** Reflection ile bir constructor'a `getDeclaredConstructor()` metodu ile erişilebilir. Sonrasında `newInstance()` metodu ile bu constructor çağrılabilir.

---

## **📌 Özet**

- **Reflection**, Java'da çalışma zamanında sınıf, metod, alan ve constructor bilgilerine erişim sağlar.
- **Class, Method, Field, Constructor** gibi sınıflar, Reflection API'sinin temel bileşenleridir.
- **Performans ve güvenlik sorunları** Reflection kullanırken dikkate alınması gereken dezavantajlardır.
- Framework'ler ve kütüphaneler genellikle **dependency injection, proxy oluşturma ve dinamik nesne yönetimi** için Reflection kullanır.
