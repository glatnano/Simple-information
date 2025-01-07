### Docker Teknolojisi Nedir?

Docker, uygulamaları **hafif, taşınabilir ve izole edilmiş bir ortamda çalıştırmak** için kullanılan bir teknolojidir. Bu ortamlar, **konteyner** (container) olarak adlandırılır. Konteynerler, bir uygulamanın çalışması için gerekli tüm bileşenleri (kod, kütüphaneler, bağımlılıklar vb.) içerir. Böylece uygulama, farklı sistemlerde aynı şekilde çalışabilir.

---

### Docker Ne İşe Yarar?

1. **Platformdan Bağımsızlık Sağlar:**
   - Docker, "Bir yerde çalışıyorsa, her yerde çalışır." mantığını benimser. Geliştiriciler, uygulamalarını kendi bilgisayarlarında çalıştırdıkları gibi, başka bir bilgisayarda, bulut ortamında veya sunucuda da çalıştırabilir.

2. **Hafif ve Hızlıdır:**
   - Docker, sanal makinelerden farklı olarak sadece gerekli bileşenleri barındırır. Bu nedenle daha hızlı çalışır ve az kaynak tüketir.

3. **Taşınabilirlik:**
   - Bir Docker konteyneri, farklı işletim sistemlerinde ve altyapılarda çalışabilir.

4. **Kolay Yedekleme ve Dağıtım:**
   - Bir uygulamanın Docker görüntüsü (image) alınarak, istenilen her yerde dağıtımı kolayca yapılabilir.

5. **Yalıtılmış Ortam:**
   - Docker, uygulamaları ve bağımlılıklarını yalıtarak, farklı uygulamaların birbirini etkilemesini önler.

---

### Docker Nasıl Kullanılır?

1. **Docker Kurulumu:**
   - Docker'ı işletim sisteminize kurun. (Windows, MacOS veya Linux için [Docker resmi sitesi](https://www.docker.com) üzerinden kurulabilir.)

2. **Docker Image ve Container:**
   - **Docker Image:** Bir uygulamanın çalışması için gereken tüm yapılandırmayı ve dosyaları içerir.
   - **Docker Container:** Bir Docker image’den oluşturulan çalışan bir ortamdır.

3. **Temel Komutlar:**
   - **Docker Image Çekmek:**  
     ```bash
     docker pull [image_adı]
     ```
     Örneğin: `docker pull nginx`

   - **Container Çalıştırmak:**  
     ```bash
     docker run [image_adı]
     ```
     Örneğin: `docker run nginx`

   - **Çalışan Container'ları Görüntülemek:**  
     ```bash
     docker ps
     ```

   - **Container'ı Durdurmak:**  
     ```bash
     docker stop [container_id]
     ```

4. **Dockerfile Kullanımı:**
   - Dockerfile, bir uygulamanın nasıl bir konteynerde çalıştırılacağını tarif eden bir dosyadır. Örnek bir `Dockerfile`:
     ```dockerfile
     FROM python:3.9-slim
     COPY . /app
     WORKDIR /app
     RUN pip install -r requirements.txt
     CMD ["python", "app.py"]
     ```
   - Bu dosya ile kendi Docker image'inizi oluşturabilirsiniz.

---

### Özet:
- **Docker**, uygulamaları yalıtılmış konteynerlerde çalıştırır.
- **Ne işe yarar?** Hızlı geliştirme, kolay dağıtım ve taşınabilirlik sağlar.
- **Nasıl kullanılır?** Docker image’ları çekerek, container’lar oluşturup uygulamaları çalıştırabilirsiniz.
