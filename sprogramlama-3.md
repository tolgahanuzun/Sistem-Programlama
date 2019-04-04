# Sistem Programlama 3. Ders

## Regular Expression (Düzenli ifade)
Bilgisayarcılıkta düzenlemeli ifadeler, ele alınan metindeki kimi katarların kısa yoldan ve esnek bir biçimde belirlenmesini sağlar. Bu katarlar belli karakterler, kelimeler veya karakter örüntüleri olabilir. Düzenlemeli ifadeler, bir biçimsel dil kullanarak yazılır ve bir düzenlemeli ifade işleyici tarafından yorumlanır. Bir düzenlemeli ifade işleyici, ya ayrıştırıcı üreteci olarak hizmet eden ya da metni inceleyip verilen tarife uygun kısımlarını belirleyen bir programdır.

- Grep : Grep’in acilimi evrensel düzenli ifade yazicisi dır. (Global Regular Expression Printer). Daha aciklayici olmak gerekirse grep , verilen bir yazidan belirli kriterler dahilinde parcalar cikarir. Basitce , grep bir sablon girmenizi , ardindan yine sizin belirleyeceginiz bir metinde, bu sablona uygun yazilari arar. Belirlenen sablona uygun tüm satirlari listeler. Grep tek başına veya borularla kullanılabilir.

``` bash
grep John /etc/passwd  # /etc/passwd dosyası içerisindeki John kelimesinin geçtiği satırları listeler.
grep -v John /etc/passwd  #/etc/passwd dosyası içersindeki John gecmeyen satırları listeleyecektir.
grep -c John /etc/passwd  #/etc/passwd dosyası içersindeki John kelimesinin dosya içerisinde kaç kez kullanıldığını listeleyecektir.
grep -i John /etc/passwd  #küçük/büyük harf duyarsızlığı oluşacaktır.
grep -r John /home/users # belirttiğiniz klasörde ve tüm alt klasörlerinde arama yapacaktir.
```
- Egrep: Egrep komutu yardımıyla, ''+'' işaretiyle biten ifadeler bir veya daha fazla sayıda karşılaştırılabilir. Buna karşılık ''-'' işareti ile biten ifadeler sıfır veya bir kere karşılaştırılabilir. Birbirinden ''|'' veya newline karakteri ile ayrılmış ifadelerden biri veya diğeri karşılaştırma işlemine sokulabilir. Son olarak, bu ifade parantez içine alınarak gruplandırılabilir. 

## Metacharacters ( Özel Karakterler)
    $ ‘ ’ “ ” ~ & | <<<>>> () {} * ? [] \ .
Yukarda bulunan karakterler ile başlayan ya da içinde geçen ya da biten dosya isimleri sakıncalıdır. Sebebi linuxün kendi sistemi içinde yukardaki her bir karaktere özel bir anlam yüklemesindendir.

- '.' = Nokta karakteri Regex için tek bir karakteri bildirir.
- '*' = Yıldız karakteri Regex için kendinden önce gelen ya hiç karakter yoktur yada o karakterlerden birden fazla olabilir.
- '+' = Plus karakteri Regex için kendinden önce gelen karakterden en az 1 yada daha fazla gelmesi kosuludur.
- '?' = Soru isareti Regex için kendinden önce gelen karakter için ya var ya da yok anlamı taşır. "if statement"
- '|' = Soru isareti gibi if anlami tasir. Ancak bir harf icin degil tum kelime grubu icin gecerlidir.
- '^' = Karet (Düzeltme İşareti) satir basindan itibaren arama yapmayi saglar.
- '$' = Dolar isareti satirin sonunu isaret eder.
- '\\' = BackSlash Metacharacters ifadelerini aramak isteyenler icin bir kacis karakteridir.
- '[]' = Köşeli parantez bir karakter dizisinde veri seçmenizi sağlar.
- '[^]' = Köşeli parantezde koret isareti programlama dillerindeki 'not' yani degili ifadesine esittir.
- '()' = Parantez birden fazla veriyi Metacharacters ile kontrol etmeye yarar.

``` bash
ls a.c # abc,adc,a&c vb.. 
ls u..x # unix, unax, ussx vb.
ls ab*c # ac, abc, abbc
ls ab?c # ac veya abc
ls ab|cd # ab veya cd
ls ^D.* # D ile baslayan butun dosyalar doner. Burada ^ satir basini ifade eder. Yildiz ise kendisinden onceki karakterin birden fazla olacagini soyler. Kendinden onceki karakter ise nokta oldugu icin gelebilecek karakterlerde herhangibi bir char veri gelebilir diyebiliriz.
ls .*d$ # d ile biten dosyalar doner. Yukaridaki mantigin aynisidir.
egrep "a\." BASH # Bash icerisinde 'a.' iceren ifadeler doner. 'tolga.' gibi.
ls [ab]c # ac veya bc isimli dosya varsa ls yapar.
ls [^ab]c # ac ve bc isimli dosya haric diger veriler geri doner. (cc,dc,fc vs..)
ls a(bc)* # a,abc,abcbc,abcbcbc vs..

```
