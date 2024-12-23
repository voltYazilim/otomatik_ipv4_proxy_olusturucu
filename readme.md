# Squid Proxy Kurulumu

Bu script, Squid Proxy sunucusunu otomatik olarak kurar ve yapılandırır. Aşağıdaki adımları izleyerek kurulumu gerçekleştirebilirsiniz.

## Gereksinimler
- Ubuntu 20.04 veya daha yeni bir sürüm
- Root erişimi veya sudo yetkisi

## Kullanım

1. **Script'i indirin:**

    ```bash
    wget -O setup_script.sh https://raw.githubusercontent.com/voltYazilim/otomatik_ipv4_proxy_olusturucu/refs/heads/main/index
    ```

2. **Çalıştırma izni verin:**

    ```bash
    chmod +x setup_script.sh
    ```

3. **Script'i çalıştırın:**

    ```bash
    ./setup_script.sh
    ```

## Script'in Yaptıkları

- Squid Proxy ve gerekli bağımlılıkları yükler.
- Mevcut Squid konfigürasyon dosyasını yedekler.
- HTTPS proxy yapılandırmasını hazırlar.
- Kullanıcı doğrulama mekanizması ekler.
- Firewall ayarlarını yapılandırır.

## Varsayılan Kullanıcı Bilgileri
- **Kullanıcı Adı:** `volt`
- **Şifre:** `master34`

## Notlar
- Script çalıştırıldıktan sonra sunucunuz HTTPS Proxy olarak çalışmaya hazır olacaktır.
- Kullanıcı bilgilerini değiştirmek isterseniz, aşağıdaki komutu kullanabilirsiniz:

    ```bash
    sudo htpasswd /etc/squid/passwd <yeni_kullanıcı_adı>
    ```

Herhangi bir sorunla karşılaşırsanız, [GitHub Issues](https://github.com/voltYazilim/otomatik_ipv4_proxy_olusturucu/issues) kısmından destek alabilirsiniz.
