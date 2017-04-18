# BASH
## Değişkenler
- Yerel degişkenleri - a,b,c ....
- Ortam değişkenleri - PATH, USER ....
- Shell değişkenleri - $0, $* ....

* Shell için kendi ortam değişkenlerinizi yaratabilirsiniz. Bunları görmek için ise komut satırına _env_ yazmanız yeterlidir.
* "man ls" komutu ile dosyalama aracının detaylarına ulaşabilirsiniz. Diğer komutlarıda man komutu ile analiz edebilirsiniz.

``` bash
HOSTNAME #komutu ile makinenin ismini görebilirsiniz. --> Tolgahans-MacBook-Air.local
echo bubirprintifadesidir # Ekrana bubirprintifadesidir basar.
echo $UID #User id --> 501
echo $PPID #Parant process id --> 12441
echo $$ #Shell id --> 12442 
ps #Bash id --> 12440
echo $RANDOM #Random bir sayi ekrana basar -> 24384
echo $HISTFILE #Gecmis dosyasini gosterir -> /Users/tolgahanuzun/.zsh_history
echo $HISTSIZE # 60 saniye boyunca dosya boyutunu kontrol eder.
echo $PS2 # komut satirini ekrana basar
```

- NOT: Ben shell olarak ZSH kullanıyorum. Bu bana BASH üzerine daha kabiliyetli imkanlar sunuyor. Sizde BASH kullanabilir veya kullandığınız işletim sistemine özel olaral farklı shell türlerini deneyebilirsiniz.

- Alias: Shellin kendine ozgu komutlaridir. Bende zsh oldugu icin bazı kolaylıklar bulunuyor. Bash için "cd .. " komutu benım shellımin özelliği ile sadece ".." ile gerçekleşiyor. Başka bir örnek ise; "ggpush" kısaltması 'git push origin $(git_current_branch)' karşılık gelir. Sizde kendiniz bu tarz komutlar yaratabilirsiniz.

## BASH Dosya Anlamları

- /etc/profile # Giriş yapılan üyeliğin dosya bloğu
- ~/.bash-profile #Gecerli profil ayarları
- ~/.bash-login #Sistem login olunca koşulacak kodlar
- ~/.profile
- ~/.bashrc
- ~/.bash-logout # Sistem logout olunca koşulacak kodlar
