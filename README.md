# İçindekiler

* [Sistem Programlama](#sistem-programlama)
    * UNIX ve Tarihçesi
    * Shell'e Giriş ve örnek komutlar (who-date-ls-echo)

* [Sistem Programlama - 1](./sprogramlama-1.md)
    * UNIX Dosyalama Sistemi
    * UNIX ve LINUX için Dosya yollari ve anlamlari
    * UNIX Basit Komutlar (pwd-cd-touch-mv-cp-rm-mkdir)

* [Sistem Programlama - 2](./sprogramlama-2.md)
    * Text Editör
    * Shell Programlama
    * UNIX Detaylı Komutlar 



# Sistem-Programlama

Bu repoda Karadeniz Teknik Üniversitesi Bilgisayar Mühendisliği Bölümü 3.Sınıf; Sistem Programlama dersi dökümantasyonu bulunmaktadir. Hatalı / eksik gördüğünüz yerleri issues ile bildirebilir veya kaynağa destek olmak amacıyla direk Pull Requests atabilirsiniz.


## Neden UNIX?
- UNIX türevi işletim sistemleri çok işlemcili çok pahalı makinalardan, tek işlemcili basit ve çok ucuz ev bilgisayarlarına kadar pek çok cihaz üzerinde çalışabilen esnek ve sağlamlığı çok değişik koşullarda test edilmiş sistemlerdir.

## UNIX'in tarihçesi?
- 1960 yılında MIT, AT&T Bell Teknoloji Laboratuvarları ve GE(General Electric)'nin birlikte geliştirdikleri MULTICS (Multiplexed Operating and Computing System [Çoğullandırılmış İşletim ve Bilgisayar Sistemi]) projesiyle temelleri atılmıştır. 
- Hedef kitlesi bilgisayar uzmanlarıdır.
- %95'lik kısmı C, %5'lik kısmı ise Assembly ile yazılmıştır.
- 1978 yılı Unix için çok önemli bir yıl olarak geçti. Unix İşletim Sistemi 7. sürümüyle birlikte gelişimini artık iki farklı çizgide gerçekteştirecekti: BSD(Berkeley Software Distribution) ve System V.

## UNIX structure

* Kernel: UNIX işletim sisteminin çekirdeğidir. Düşük seviyeli fonksiyonları ve donanımı kontrol eder.

* Shell: Kullanıcı ve sistem etkileşimini kontrol eder. Kullanıcıların komutlarına cevap verir.

## Shell Nedir?

- Komut yorumlayıcısıdır. Verilen parametreleri değerlendirir. Ardından programın çalışmasını sağlar. 
- Bir programlama dilidir.
- Shell komutlarını içeren programlara 'shell script' denir.

## Shell'e Giriş.

- En yetkili üyelik her zaman Root'dur. Gerekli izinleri Root yetkisi ile ayarlanır. Bazı özel işlemler için Root yetkisi sorar ve password ile koruma altına alır. Bazı dosyaları ve dizinleri silmek gibi işlemlerde bununla karşılaşmak mümkündür.

### Shell için örnek komutlar. 
- Bazı komutlar için çıktılarınıda paylaşarak örneklendirmeye çalışacağım. Parametre alan yapılar için örnek parametre olarak 'ktuceng' tagını kullanacağım.

``` bash
who # Sistemde çalışan aktif kullanıcıları listeler.
date # Sistemin saatini geri döndürür.
ls # Bulunduğunuz noktadaki dizin yapısını döker. Klasörler ve dosyalar... Ayrıca -l gibi parametreler ile özelleştirmek ve detaylandırmak mümkünüdür.
echo ktuceng # Kendisinden sonraki veriyi ekrana basar.
pwd # Bulunduğunuz dizini geri döndürür.
CTRL-c # Çalışan programı sonlandırır. 
CTRL-z # Çalışan programı bir süreliğine durdurur. Tekrar tuşlara basıldığında çalışmasına devam ettirilir.
CTRL-d # Çalışan programı zorlar ve terminalden bağlantısını koparır. 
```
    who:    
    tolgahanuzun console  Mar 18 23:29
    tolgahanuzun ttys000  Apr  7 02:57

    date:    
    Fri Apr  7 03:59:14 MSK 2017

    ls:
    README.md static

    echo: 
    ktuceng

    pwd:
    /Users/tolgahanuzun/Github/dersler/sistemprogramlama


