Açıklamalı Liste

    exec: Sistemde komut çalıştırmak için kullanılır. Bir saldırgan, sunucuda komut çalıştırarak ciddi zararlar verebilir.

    passthru: Sistemde komut çalıştırır ve çıktısını doğrudan verir. Saldırganlar bu fonksiyonu kullanarak kötü amaçlı komutları doğrudan sunucu üzerinde çalıştırabilirler.

    shell_exec: exec gibi çalışır ancak tüm çıktıyı bir dize olarak döner. Komut satırı komutlarının çalıştırılmasına izin verir, bu da güvenlik riski doğurur.

    system: Sistemde bir komut çalıştırır ve komutun çıktısını ekrana basar. Kötü niyetli kullanıcılar bu fonksiyon aracılığıyla sistemde yetkisiz komutlar çalıştırabilir.

    proc_open: Sistemde bir işlem başlatır ve girdi/çıktı akışlarını yönetir. Saldırganlar, bu fonksiyonu kullanarak kötü amaçlı işlemler başlatabilir.

    popen: proc_open benzeri bir fonksiyon olup bir komut çalıştırır ve bu komutun giriş/çıkış akışlarını yönetir. Güvenlik riski barındırır.

    curl_exec / curl_multi_exec: Dışarıya HTTP istekleri göndermeye izin verir. Kötü yapılandırılmış bir sistemde saldırganlar istek yaparak hassas verileri ele geçirebilir veya zararlı içerik çekebilirler.

    parse_ini_file: Bir INI dosyasını ayrıştırır ve bu dosyalardan veri okur. Hassas yapılandırma dosyalarını açığa çıkarabilir.

    show_source: PHP dosyasının kaynak kodunu gösterir. Kötü niyetli kullanıcılar bu fonksiyon sayesinde kritik dosyaların kaynak kodlarına erişebilirler.

    phpinfo: PHP’nin yapılandırma bilgilerini gösterir. Saldırganlara sunucunuzun güvenlik açığına dair bilgi verebilir (örneğin, yüklü modüller, dizin yapısı).

    mail: Sunucudan e-posta göndermek için kullanılır. Düzgün güvenlik önlemleri olmadan kullanıldığında spam saldırılarına yol açabilir.

    ini_set / ini_alter: PHP yapılandırma ayarlarını dinamik olarak değiştirmeye izin verir. Saldırganlar bu fonksiyonları kullanarak PHP'nin çalışma şeklini değiştirebilirler.

    openlog / syslog: Loglama fonksiyonlarıdır. Bir saldırgan, bu fonksiyonlar aracılığıyla logları manipüle edebilir veya logları kullanarak sisteme dair bilgi edinebilir.

    readfile: Bir dosyanın içeriğini okur ve çıktı olarak verir. Hassas dosyaların içeriğinin açığa çıkmasına neden olabilir.

    symlink: Sembolik linkler oluşturur. Bir saldırgan, bu fonksiyonu kullanarak yetkisiz dosyalara erişim sağlayabilir.

    dl: Yükleme zamanı paylaşılan bir PHP uzantısı yükler. Bu fonksiyon, genellikle güvenlik açıklarına yol açan dinamik uzantı yüklemeleri için kullanılabilir.

    leak: Hafıza sızıntılarını test etmek için kullanılır. Bu fonksiyon, saldırganların sistem kaynaklarını tükenmesine neden olabilir.

    proc_get_status / proc_terminate: Çalışan bir işlem hakkında bilgi verir veya bir işlemi sonlandırır. Bu fonksiyonlar, saldırganların mevcut işlemleri manipüle etmelerine olanak tanır.

    posix_kill / posix_mkfifo / posix_setpgid / posix_setsid / posix_setuid: Bu fonksiyonlar POSIX işlemleriyle ilgilidir ve bir işlem yönetme yetkisi verir. Bu da saldırganların sisteme zarar vermesine yol açabilir.

    escapeshellarg / escapeshellcmd: Kabuk argümanlarını güvenli hale getirmek için kullanılırlar, ancak kötü kullanıldıklarında saldırganlar bu mekanizmaları aşabilirler.

    base64_decode: Base64 ile kodlanmış bir dizeyi çözer. Bu, zararlı kodların gizlenmesinde kullanılabilir.

Öneriler:

    PHP Fonksiyonlarını Devre Dışı Bırakmak: Eğer bu fonksiyonlara ihtiyaç duymuyorsanız, sunucu yapılandırma dosyasında (php.ini) disable_functions direktifi ile devre dışı bırakılmaları güvenlik açısından tavsiye edilir.

    Kapsamlı Test: Fonksiyonları devre dışı bırakmadan önce, uygulamanızın bu fonksiyonlara ihtiyaç duyup duymadığını test edin. Bazı uygulamalar bu fonksiyonlara güvenebilir.
