# 🧩 Java Annotations

---

## 🎯 1. Annotation Nedir?

> Annotation, Java’da sınıf, metot, değişken veya parametreler hakkında  
> **ek bilgi (metadata)** vermek için kullanılan yapılardır.

- Annotation’lar doğrudan iş mantığı içermez.
- Derleyici, framework veya runtime tarafından okunur.

---

## 🧠 2. Neden Önemlidir?

✔ Kod tekrarını azaltır  
✔ Okunabilirliği artırır  
✔ Framework’lerin (Spring, JUnit) temelini oluşturur  
✔ XML yerine kod üzerinden konfigürasyon sağlar  

---

## 🧩 3. Annotation Türleri

---

### 3.1 Built-in (Hazır) Annotations

Java ile birlikte gelen annotation’lardır.

---

#### 🔹 `@Override`
> Bir metodun üst sınıftaki metodu override ettiğini belirtir.

#### 🔹 `@Deprecated`
> Kullanımı önerilmeyen kodu işaretler.

#### 🔹 `@SuppressWarnings`
> Derleyici uyarılarını bastırır.

---

#### 📌 Örnek
```java
@Override
public String toString() {
    return "User";
}

---

3.2 Meta-Annotations

Annotation’ların nasıl kullanılacağını belirler.

🔹 @Target

Annotation’ın nerede kullanılacağını belirtir
(class, method, field vb.)

🔹 @Retention

Annotation’ın ne zamana kadar geçerli olduğunu belirtir.

🔹 @Documented

Javadoc içerisine eklenmesini sağlar.

🔹 @Inherited

Alt sınıflara miras kalmasını sağlar.


📌 Örnek

import java.lang.annotation.*;

@Target(ElementType.METHOD) // Sadece metotlarda kullanılabilir
@Retention(RetentionPolicy.RUNTIME) // Runtime'da okunabilir
@Documented
@Inherited
public @interface MyAnnotation {
}


---

⏱ 4. Retention Policy

Annotation’ın yaşam süresini belirler.

🔸 SOURCE

Sadece yazım sırasında vardır

Compile sonrası silinir

🔸 CLASS

Compile edilir

Runtime’da erişilemez

🔸 RUNTIME

Çalışma zamanında erişilebilir

⚠️ Spring annotation’ları genellikle RUNTIME kullanır.

---

🛠 5. Custom Annotation (Özel Annotation)

Geliştirici kendi annotation’ını yazabilir.

📌 Örnek

import java.lang.annotation.*;

@Target(ElementType.METHOD)
@Retention(RetentionPolicy.RUNTIME)
public @interface LogTime {
    String value();
}


📌 Kullanımı

public class PaymentService {

    @LogTime("Ödeme işlemi süresi ölçülüyor")
    public void pay() {
        System.out.println("Payment completed");
    }
}



🌱 6. Spring Framework’te Annotation Kullanımı

Spring, annotation tabanlı çalışır.

🔹 Sık Kullanılan Annotation’lar

@Component
Spring tarafından yönetilen bir bean tanımlar.

@Service
İş mantığı içeren sınıflar için kullanılır.

@Repository
Veritabanı katmanını temsil eder.

@Controller
MVC controller sınıflarında kullanılır.

@RestController
REST API geliştirmek için kullanılır.

@Autowired
Dependency Injection sağlar.

@GetMapping
GET isteklerini karşılar.

📌 Örnek

@RestController
@RequestMapping("/api/users")
public class UserController {

    @Autowired
    private UserService userService;

    @GetMapping("/{id}")
    public User getUser(@PathVariable Long id) {
        return userService.getUser(id);
    }
}

⚠️ 7. Sık Yapılan Hatalar

❌ Annotation ile iş mantığı yazmak
❌ Yanlış RetentionPolicy seçmek
❌ Her yere @Autowired eklemek
❌ Annotation’ın ne zaman okunduğunu bilmemek

✅ 8. Özet

Annotation’lar, Java ve Spring dünyasında
konfigürasyonu sadeleştiren ve kodu okunabilir hale getiren yapılardır.

Doğru yerde kullanıldığında
hem geliştirme hem test süreçlerini kolaylaştırır.

