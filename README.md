# Basit SQL Injection Vulnerable PHP Web Uygulaması - Eğitim Amaçlı

Bu proje, **SQL Injection (SQLi)** açığını anlamak ve pratik yapmak isteyenler için hazırlanmış basit bir PHP web uygulamasıdır. İçinde **bcrypt ile hashlenmiş bir parola** bulunmakta ve bu parola **nerede olduğu bilinmeden** kullanıcı tarafından bulunması hedeflenmektedir.

---

## Proje Özellikleri

- PHP ve MySQL/MariaDB ile geliştirilmiş basit yapı
- `login.php` sayfasında SQL Injection açığı barındırır
- Veritabanında bcrypt ile hashlenmiş parola bulunur
- Zafiyet testi ve eğitim için uygun kolay seviye
- Kullanımı kolay, hızlı kurulabilir

---

## Kurulum ve Kullanım

1. Projeyi indirin ve sunucunuzun web dizinine çıkartın(zip ile indirenler icin):

   ```bash
   unzip sql_vulnerable_site.zip -d /var/www/html/sql_lab
   ```
2. Apache ve MySQL servislerini başlatın:

   ```bash
   sudo service apache2 start
   sudo service mysql start
   ```

3. Veritabanını yükleyin:

   ```bash
   sudo mysql -u root < /var/www/html/sql_lab/db.sql
   ```

4. Tarayıcıdan siteyi açın:

   ```
   http://localhost/sql_lab/
   ```

5. URL’ye `login.php?id=1` gibi parametrelerle erişin.  
   Burada `id` parametresi sorguda doğrudan kullanıldığı için SQL Injection açıktır.  
   Farklı payloadlarla veritabanından veri çekmeyi deneyin.
### Alternatif Kurulum: Git Clone ile

1. Projeyi zip indirmek yerine doğrudan GitHub’dan klonlamak için:

```bash
git clone https://github.com/TrollO-droid/sql-injection-training-lab.git
```
2. Klonlanan dosyaları Apache web dizinine kopyalayın:

```bash
sudo mkdir -p /var/www/html/sql_lab
sudo cp -r sql-injection-training-lab/* /var/www/html/sql_lab/
```
3. Veritabanını yükleyin:

   ```bash
   sudo mysql -u root < /var/www/html/sql_lab/db.sql
   ```

4. Tarayıcıdan siteyi açın:

   ```
   http://localhost/sql_lab/
   ```
5. URL’ye `login.php?id=1` gibi parametrelerle erişin.  
   Burada `id` parametresi sorguda doğrudan kullanıldığı için SQL Injection açıktır.  
   Farklı payloadlarla veritabanından veri çekmeyi deneyin.
---

## Amaç

- SQL Injection açığını anlamak ve pratik yapmak.
- Hashlenmiş parola nerede olduğunu bulmak ve sifreyi bulmak.
- Web güvenliği ve penetrasyon testi eğitimi için temel olusturmak.

---

## Notlar
  
- Hash olarak kullanılan parola: `Password123`'ün bcrypt versiyonudur.  

---

Created By Troll

---

