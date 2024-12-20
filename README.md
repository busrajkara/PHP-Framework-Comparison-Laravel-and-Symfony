# Framework Nedir?

Bir framework, yazılım geliştirmeyi kolaylaştırmak için hazırlanmış bir araç setidir. Düşün ki bir ev yapıyorsun; framework, hazır bir iskelet veya plan sunar, böylece duvarları ve çatıyı sıfırdan inşa etmek zorunda kalmazsın. Özellikle PHP dilinde, frameworkler:
- **Kod düzenini** sağlar (her şey yerli yerinde!),
- **Hata yönetimini** kolaylaştırır (yanlış yaparsan, sana neyi düzelteceğini söyler!),
- **Güvenlik** sağlar (evin kapısı sağlam!),
- **Projeyi büyütmeyi kolaylaştırır** (daha büyük bir ev yapmak istersen uygun bir plan hazır!).

---

# Laravel ve Symfony Nedir?

## Laravel
Laravel, PHP ile çalışan bir yazılım frameworküdür. Kullanımı kolay ve modern projeler yapmak için idealdir. Laravel, **MVC (Model-View-Controller)** denilen bir yapıyı kullanır (bu, kodunu düzenli tutmak için kullanılan bir yöntemdir).

### Özellikleri:
- **ORM (Eloquent)**: Veritabanıyla kolayca konuşmanı sağlar (düşün, bilgisayar dilinden insan diline çeviriyor!).
- **Blade templating engine**: Web sayfanın görünüşünü düzenlemek için kullanılır (sihirli bir fırça gibi!).
- **Artisan CLI**: Komut satırında işler yapmanı kolaylaştırır (tek bir komutla projeni hızlandır!).
- **Görev zamanlayıcı**: Belli işleri otomatik olarak belli bir zamanda yapar (bir alarm gibi düşün!).
- **Basit rota tanımlamaları**: Projendeki yolları kolayca tanımlarsın (haritayı hızlıca çizmek gibi!).

> **Not:** Laravel, hızlı sonuç almak isteyenler ve çok fazla teknik bilgiye sahip olmayanlar için daha uygundur.

## Symfony
Symfony, PHP için hazırlanmış daha karmaşık ve esnek bir frameworktür. Daha büyük ve daha ciddi projeler için tercih edilir. Laravel gibi, Symfony de web uygulamaları yapmak için kullanılır, ama daha çok bir "araç kutusu" gibidir. İçinden sadece ihtiyacın olanı alabilirsin!

### Özellikleri:
- **Bağımsız bileşenler**: Her bir parçası tek başına kullanılabilir (bir Lego seti gibi!).
- **Esnek yapı**: İhtiyacına göre düzenleyebilirsin (her türlü projeye uygun hale gelir!).
- **Twig templating engine**: Web sayfanın tasarımını düzenlemek için güçlü bir araçtır.
- **Konsol komutları**: Symfony de komutlarla çalışır ama daha detaylı işler yapar.
- **Gelişmiş güvenlik araçları**: Özellikle kullanıcı bilgilerinin güvenliğini sağlamada çok iyi (kasası sağlam bir banka gibi!).

> **Not:** Symfony, daha fazla teknik bilgiye sahip olanlar ve büyük projeler için daha uygundur.

---

# Laravel ve Symfony Karşılaştırması

| **Kriter**        | **Laravel**                              | **Symfony**                                   |
|--------------------|------------------------------------------|-----------------------------------------------|
| **Öğrenme Eğrisi** | Öğrenmesi kolay. Hızlı başlamak istersen iyi bir seçim. | Öğrenmesi daha zor ama daha esnek bir yapı sunar. |
| **Performans**     | Küçük ve orta ölçekli projelerde yeterli performans sunar. | Büyük projelerde daha hızlı ve güçlü çalışır. |
| **Topluluk**       | Çok büyük bir topluluğu var. Yardım bulmak kolay. | Daha kurumsal ve profesyonel bir topluluğa sahip. |
| **Bileşen Kullanımı** | Her şey bir arada. Başlangıç için daha basit. | Modüler yapı. İhtiyacın kadarını alabilirsin. |
| **Kod Düzeni**     | Kodlar basit ve hızlı yazılır.            | Kodlar biraz daha karmaşık ama uzun vadede esnek. |
| **Proje Türü**     | Küçük ve orta ölçekli projeler için ideal. | Büyük, uzun vadeli projeler için harika.      |

### Notlar:
- Eğer bir projeye hızlıca başlamak ve kolayca bitirmek istiyorsan: **Laravel**.
- Eğer büyük bir proje yapacaksan, gelecekte genişlemesi gerekirse: **Symfony**.
- Laravel daha çok bir Lego evi yapmak gibi, her şey hazır geliyor.
- Symfony ise kendi Lego parçalarını seçip istediğin evi yapmak gibi, daha özgürsün ama biraz daha uğraşman gerekebilir.

## --------------------------------------------------------------------------------------------------

# Laravel Projesi Başlatma

Laravel projesini başlatmak için aşağıdaki adımları takip edebilirsiniz.

## Gerekli PHP Eklentileri
Aşağıdaki PHP eklentilerinin aktif olması gereklidir:

- **sqlite**
- **pdo_sqlite**
- **file_...** (ilgili dosya işlemleriyle ilgili bir eklenti)

Eklentilerinizi kontrol etmek için `phpinfo()` veya `php -m` komutlarını kullanabilirsiniz.

## Projeyi Çalıştırma

1. **Laravel Projesini Başlat**  
   ```bash
   php artisan serve
   ```

2. **Node.js Bağımlılıklarını Yükle**  
   Projenizde bir `package.json` dosyası bulunduğu için `npm install` çalıştırarak gerekli bağımlılıkları yükleyin:  
   ```bash
   npm install
   ```

---

## Sqlite Hatası Aldık

### Hata:
Eğer aşağıdaki gibi bir SQLite hatasıyla karşılaşırsanız:

```plaintext
SQLSTATE[HY000]: General error: 1 no such table: sessions (Connection: sqlite, SQL: select * from "sessions" where "id" = nP0nQ4xISlb3C8o6KVpl86TUj7QplAi8G0QNw624 limit 1)
```

### Çözüm:

1. **Veritabanı Tablolarını Oluştur**  
   Eğer tablolar henüz oluşturulmamışsa, aşağıdaki komutu çalıştırın:  
   ```bash
   php artisan migrate
   ```

2. **Tabloları Yeniden Oluştur**  
   Eğer tablolar mevcutsa ve sıfırlamak istiyorsanız:  
   ```bash
   php artisan migrate:fresh
   ```

---

### Ekstra Notlar
- `php artisan migrate` komutu, veritabanı tablolarını oluşturur veya eksik tabloları tamamlar.
- `php artisan migrate:fresh` komutu, mevcut tabloları silerek sıfırdan oluşturur.

Bu adımları izleyerek projeyi sorunsuz bir şekilde çalıştırabilirsiniz.
