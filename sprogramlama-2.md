# Sistem Programlama 2. Ders

## Text Editor
Unix bir bilgisayara genellikle SSH üzerinden terminal ile bağlandığımız için bu bilgisayara GUI anlamında bir görsel temasımız bulunmaz. Yani SSH ile bağlandığımız bilgisayarı terminal üzerinden kontrol ederiz. Bu aşamada ulaştığımız terminalde veri oluşturmak ve verileri değiştirmek için temel anlamda "Vİ" yada daha güncel hali olan "VİM" text editörü tercih edilebilir. Bunun farklı alternatifleri de vardır. Ancak en popüleri ve unix bilgisayarda kurulu olarak geldiği için vi text editörlü tercih edilmektedir.

``` bash
vi ktuceng.txt # Bulundugumuz dizinde bu adda bir dosya önceden oluşturulmuştur.
vi olmayandosya.txt # Böyle bir dosya hiç oluşturulmadı.
```
* Yukarıdaki ilk kodda önceden var olan dosya üzerinde değiştirilme işlemleri için dosya vi editörü aracılığı ile açılır.
* İkinci kodda ise dizinde bulunmayan bir dosya vi editörü tarafından kendiliğinde yaratılır ve içerisine veri girmeniz için size yetki verir.

## Shell Programlama

### Shell Nedir?
Linux'un türetildiği UNIX sistemlerinde komutları yorumlamak ve yönetmek için kullanılan programa kabuk denir. Bir başka değişle bilgisayar ekranımızın yönetimini pencereler ve simgeler ele geçirmeden önce bilgisayarlarımızı çalıştırmak için kullandığımız komutları yazdığımız bir tür paneldir.

Bütün LINUX dağıtımlarında bir kabuk bulunur. Bir başka değişle Kabuk bir LINUX sistemin olmazsa olmazıdır. 

### Shell Programlama
Shellde yaptığımız herşey bir dosya gibi düşünebiliriz. Bununla beraber Shell için standart bir dosyalama yapısı bulunur. Bunlar:

1. Stdin = Klavyeden bilgi almak için kullanılır. (Standart Giriş)
2. Stdout = Bilgi yazmak için kullanılır. (Standart Çıkış)
3. Stderr = Hata mesajı yazdırır. (Standart Hata)

``` bash
ls > ktuceng.txt # Dizindeki dosyaları ve klasörleri ktuceng adlı dosyaya yazar. Burada yazma dosyanın başında olmaktadır.
ls >> ktuceng.txt # Dizindeki dosyaları ve klasörleri ktuceng adlı dosyanın sonuna ekler!!! Burada yazma dosyanın sonunda olmaktadır.
```

``` bash
cat ktuceng.txt > yenidosya.txt # CAT komutuyla bir dosya içi okunur ve bu içerik dosya içerisine yazılır.
cat < yenidosya.txt # yenidosya içeriği terminale bastırılır.
```

``` bash
cat ktuceng.txt > yenidosya.txt # CAT komutuyla bir dosya içi okunur ve bu içerik dosya içerisine yazılır.
cat < yenidosya.txt # yenidosya içeriği terminale bastırılır.
```
### Linux Komutları (halitalptekin/hackercamp Reposundan alınmıştır.)
- **echo**: ifadeleri ekrana basar.
```
echo "deneme"
echo $HOME
```

- **more**, **less**: içeriği fazla olan, ekrana sığmayan dosyaları görüntüler.
```
more deneme_dosya
less deneme_dosya
```

- **head**: bir dosyanın baştan itibaren istenilen sayıda satırını ekrana basar.
```
head deneme_dosya
head -1 deneme_dosya
```

- **tail**: head gibi çalışır ancak sondan itibaren ekrana basar.
```
tail deneme_dosya
tail -1 deneme_dosya
tail -f deneme_dosya
```

- **grep**: metin dosyaları içerisinde belirli değerleri aramak için kullanılır.
```
grep "kelime" deneme_dosya
grep "kelime" . -R
grep "Kelime" deneme_dosya -i
```
