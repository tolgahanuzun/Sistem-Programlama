# Sistem Programlama 1. Ders

## UNIX Dosyalama Sistemi
- Unixte herşeyi bir dosya gibi düşünebilir ve bu şekilde erişebiliriz. 
- Burada Windowstan kalan C-D-E gibi disk sistemleri bulunmaz. Bunların hepsıne aynı dizinden ulaşabiliriz. Buna 'maunt' denir.
- Unixte her kullanıcının bir kendi dizini vardır. Örnek: "/Users/tolgahanuzun/"

Unix üzerinde terminale bağlandığınızda otomatik "/Users/tolgahanuzun/" dizininden işlemlere başlarsınız. Farklı kullanıcıların dizinine ulaşmak için "cd" yardımı ile hareket edebilirsiniz. Ayrıca "~" karakteri ile ana dizin üzerinden spesifik bir dizine değiştirme şansınız vardır. Aşağıda örneklendirme mevcuttur.

``` bash
pwd # Bulunduğum dizini gösterir /Users/tolgahanuzun/Github/dersler/sistemprogramlama
cd .. # Bulunduğum dizinden bir aşağıya gönderir. /Users/tolgahanuzun/Github/dersler
cd . # Bulunduğunuz dizinde kalmanız sağlar. Birşey olmaz.
cd ~/example/pythonderslerim # /Users/tolgahanuzun/example/pythonderslerim nerede olursanız olun, sizi buraya gönderir.
```

### UNIX ve LINUX için Dosya yollari ve anlamlari
- /bin: Kullanıcı ve sistem yöneticisine ait çalıştırılabilir dosyaları barındırır.
- /dev: Donanımlara erişebilmek için gerekli dosyaları barındırır.
- /etc: Sistem konfigürasyonları için gerekli dosyaları barındırır.
- /lib: Sistem kütüphanelerini barındırır.
- /sbin: Sistem yöneticisine ait çalıştırılabilir dosyaları barındırır.
- /home: Kullanıcılara ait dizindir.
- /mnt: Sisteme dışarıdan bağlanacak olan donanım aygıtlarının, bağlantı noktalarını belirten dizindir.
- /root: Bir sistemde en yetkili kullanıcı olan "root" kullanıcısına ait dizindir.
- /tmp: Geçici dosyaların yer aldığı dizindir.
- /usr: Paylaşılan dosyaların barındığı dizindir. Burada çalışabilen dosyalar bulunmakla beraber, döküman ve programlara ait dosyalar da yer almaktadır.
- /var: Sistem ve programlara ait log mesajları, email gibi mesajların bulunduğu dizindir.
- /proc: Sistem hakkında gerekli bilgilerin bulunduğu sanal dizindir.

### UNIX Basit Komutlar (touch-mv-cp-rm-mkdir)
``` bash
touch ktuceng.txt  #Ktuceng.txt adında bir text dosyası oluşturur. Aynı mantıkla '.c', '.py', '.rb', '.js' vb. şeklinde dosya uzantıları oluşturulabilir.
mv ktuceng.txt ceng.txt # Dizin değiştirmeden yapılan işlemlerde isim değiştirme anlamında kullanılır.
mv ktuceng.txt ./dersler # Dersler dizinine aynı işimle taşır.
mv ktuceng.txt ./dersler/ceng.txt # Dersler dizinine isim değiştirerek taşır.
cp sistem.txt sistemprogramama.txt # Sistem adlı dosya kopyalanır ve kopyalanan dosyanın ismi sistem programlama olur.
rm sistem.txt # Sistem adındaki dosya silinir.
rm -rv ./dersler # Dersler adındaki klasör ve altındaki dosyalar silinir.
mkdir dersler # Bulunduğu dizine yeni bir alt dizin oluşturur. İsmi ise dersler olur.
```