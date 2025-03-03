# Linux-a-Giris

*Komut dosyalar hakkında bilgi listesi "ls"  görüntüler


*Bir argüman, komutun üzerinde işlem yapacağı bir şeyi belirtmek için kullanılabilir. Komuta lsargüman olarak bir dizinin adı verilebilir ve bu dizinin içerikleri listelenir. Bir sonraki örnekte, dizin Documentsargüman olarak kullanılacaktır:
Örnek olarak;

sysadmin@localhost : ~ $ ls Belgeler
 Okul            alpha-second.txt food.txt linux.txt os.csv
 İş              alpha-third.txt hello.sh longfile.txt people.csv
sıfatlar.txt alpha.txt gizli.txt newhome.txt profile.txt
alpha-first.txt hayvanlar.txt harfler.txt sayılar.txt kırmızı.txt

______________________________________________________________________________________________________________________________________________

"-l" komutunu ls ile kullanarak çıktıda listelenen her dosya hakkında daha fazla bilgi alırız:

sistem yöneticisi@localhost : ~ $ ls -l
toplam 32
drwx------ 2 sysadmin sysadmin 4096 20 Aralık 2017 Masaüstü                         
drwx------ 4 sysadmin sysadmin 4096 20 Aralık 2017 Belgeler                       
drwx------ 2 sysadmin sysadmin 4096 20 Aralık 2017 İndirmeler                       
drwx------ 2 sysadmin sysadmin 4096 20 Aralık 2017 Müzik                           
drwx------ 2 sysadmin sysadmin 4096 20 Aralık 2017 Resimler                        
drwx------ 2 sysadmin sysadmin 4096 20 Aralık 2017 Genel                          
drwx------ 2 sysadmin sysadmin 4096 20 Aralık 2017 Şablonlar                       
drwx------ 2 sysadmin sysadmin 4096 20 Aralık 2017 Videolar
________________________________________________________________________________________________________________________________________________________


*Normalde ls komutunu kullanarak çıktıları alfabetik soraya göre hazırlamış oluruz. "-r" komutu ile alfabetik sıranın tersine bir sıralama almış oluruz.


sysadmin@localhost : ~ $ ls -r
Videolar Şablonlar Genel Resimler Müzik İndirmeler Belgeler Masaüstü


__________________________________________________________________________________________________________________________________________________________

*Birden fazla seçenek aynı anda kullanılabilir, ya ayrı seçenekler olarak verilir, örneğin . -l -rya da birleştirilir, örneğin -lr. Tüm bu örneklerin çıktısı aynı olacaktır:

örn;
 ls -l -r
 ls -rl
 ls -lr

________________________________________________________________________________________________________________________________________________________________

* ls komutunda "-l" ve "-r" komutlarını birlikte kullanabiliriz ve böylece ters alfabetik listelenmiş komut dosyalarını görmüş oluruz.

sistem yöneticisi@localhost : ~ $ ls -l -r
toplam 32
drwx------ 2 sysadmin sysadmin 4096 20 Aralık 2017 Videolar                          
drwx------ 2 sysadmin sysadmin 4096 20 Aralık 2017 Şablonlar                       
drwx------ 2 sysadmin sysadmin 4096 20 Aralık 2017 Genel                          
drwx------ 2 sysadmin sysadmin 4096 20 Aralık 2017 Resimler                        
drwx------ 2 sysadmin sysadmin 4096 20 Aralık 2017 Müzik                           
drwx------ 2 sysadmin sysadmin 4096 20 Aralık 2017 İndirmeler                       
drwx------ 4 sysadmin sysadmin 4096 20 Aralık 2017 Belgeler                       
drwx------ 2 sysadmin sysadmin 4096 20 Aralık 2017 Masaüstü 

sysadmin@localhost : ~ $ ls -rl
toplam 32
drwx------ 2 sysadmin sysadmin 4096 20 Aralık 2017 Videolar                          
drwx------ 2 sysadmin sysadmin 4096 20 Aralık 2017 Şablonlar                       
drwx------ 2 sysadmin sysadmin 4096 20 Aralık 2017 Genel                          
drwx------ 2 sysadmin sysadmin 4096 20 Aralık 2017 Resimler                        
drwx------ 2 sysadmin sysadmin 4096 20 Aralık 2017 Müzik                           
drwx------ 2 sysadmin sysadmin 4096 20 Aralık 2017 İndirmeler                       
drwx------ 4 sysadmin sysadmin 4096 20 Aralık 2017 Belgeler                       
drwx------ 2 sysadmin sysadmin 4096 20 Aralık 2017 Masaüstü 


*  "-v" daha ayrıntılı bilgi istemek için kullanılır

 _______________________________________________________________________________________________________________________________________________________________________________

*  Dosya sisteminde şu anda nerede olduğunuzu keşfetmek için pwdkomut kullanılabilir.

sysadmin@localhost : ~ $ pwd
/anasayfa/sistemyöneticisi

______________________________________________________________________________________________________________________________________________________________________________________


* "~" kullanıcının ana dizininde olduğunu gösterir.

* Bulunduğumuz dizini değiştirmek için "cd"(change directory komutunu kullanırız.

 sysadmin@localhost : ~ $ cd Belgeler                                              
 sysadmin@localhost : ~/Belgeler $ 


_______________________________________________________________________________________________________________________________________________________________________________________


*Bu daha popüler işletim sistemleri gibi, bir Linux dizin yapısının da en üst seviyesi vardır. "Bilgisayarım" olarak adlandırılmaz, bunun yerine kök dizin olarak adlandırılır ve karakterle temsil edilir /. Kök dizine gitmek için, "/" karakteri komuta "cd" komutuyla argüman olarak kullanın.

sysadmin@localhost : ~/Belgeler $ cd /
 sysadmin@localhost : / $

______________________________________________________________________________________________________________________________________________________________________________________________-

*"cd" kullanıcının ana dizinine geri dönmesini sağlayan komuta argüman olarak bu yolu kullanın sysadmin.

sysadmin@localhost : / $ cd /home/sysadmin
 sysadmin@localhost : ~ $

*Çıktı olmaması komutun başarılı olduğu anlamına gelir. Devam edin ve bunu şu pwdkomutu kullanarak onaylayın:

sysadmin@localhost : ~ $ pwd                                                       
/anasayfa/sistemyöneticisi

_____________________________________________________________________________________________________________________________________________________________________________

"cd" dizin içine girmek için komutun argümanı olarak bağıl yolu kullanın Art.

sysadmin@localhost : ~/Belgeler/ $ cd Okul/Sanat
 sysadmin@localhost : ~/Belgeler/Okul/Sanat $
 

*"pwd" değişikliği onaylamak için şu komutu kullanın :

sysadmin@localhost : ~/Belgeler/Okul/Sanat $ pwd                                      
/home/sysadmin/Belgeler/Okul/Sanat



_______________________________________________________________________________________________________________________________________________________________________________

*Bulunduğunuz dizinden bir önceki dizine geçmek istiyorsak "cd .." komutunu kullanırız

sysadmin@localhost : ~/Belgeler/Okul/Sanat $ cd ..                                
 sysadmin@localhost : ~/Belgeler/Okul $



*Herhangi bir zamanda ana dizinimize dönmek istiyorsak "cd ~" komutunu kullanırız.

sysadmin@localhost : ~/Belgeler/Okul $ cd ~
 sysadmin@localhost : ~ $



__________________________________________________________________________________________________________________________________________________________________________________

*Bir dosyanın türü, izinleri, sahiplikleri veya zaman damgası gibi ayrıntıları öğrenmek için, -lkomutun seçeneğini kullanarak uzun bir listeleme yapın ls. Aşağıda, çeşitli çıktılar sağladığı için bir örnek olarak dizinin bir listesi /var/logkullanılmıştır:

sysadmin@localhost : ~ $ ls -l /var/log/
toplam 844                                                                       
-rw-r--r-- 1 kök kök 18047 20 Aralık 2017 alternatifler.log                   
drwxr-x--- 2 root adm 4096 20 Aralık 2017 apache2                             
drwxr-xr-x 1 root root 4096 20 Aralık 2017 apt                                
-rw-r----- 1 syslog adm 1346 2 Ekim 22:17 auth.log                           
-rw-r--r-- 1 kök kök 47816 7 Aralık 2017 bootstrap.log                      
-rw-rw---- 1 kök utmp 0 7 Aralık 2017 btmp                               
-rw-r----- 1 syslog adm 547 2 Ekim 22:17 cron.log                           
-rw-r----- 1 kök yönetici 85083 20 Aralık 2017 dmesg                              
-rw-r--r-- 1 kök kök 325238 20 Aralık 2017 dpkg.log                           
-rw-r--r-- 1 kök kök 32064 20 Aralık 2017 başarısız günlüğü                            
drwxr-xr-x 2 kök kök 4096 7 Aralık 2017 fsck                               
-rw-r----- 1 syslog adm 106 2 Ekim 19:57 kern.log                           
-rw-rw-r-- 1 root utmp 292584 2 Eki 19:57 lastlog                            
-rw-r----- 1 syslog adm 19573 2 Ekim 22:57 syslog                             
drwxr-xr-x 2 root root 4096 11 Nis 2014 yeni başlayan                            
-rw-rw-r-- 1 kök utmp 384 2 Ekim 19:57 wtmp




*Dosya Türü

- rw-r--r-- 1 kök kök 18047 20 Aralık 2017 alternatifler.log       "-"
            
d rwxr-x--- 2 root adm 4096 20 Aralık 2017 apache2                 "d"

***İlk dosya alternatives.lognormal bir dosya iken -, ikinci dosya apache2bir dizindir d.

İlk alan aslında on karakter içerir, burada ilk karakter dosyanın türünü belirtir ve sonraki dokuz karakter izinleri belirtir. Dosya türleri şunlardır:

Sembol	    Dosya Türü         	Tanım
"d"	            dizin	          Başka dosyaları saklamak için kullanılan dosya.
"-"           düzenli dosya   	Okunabilir dosyalar, resim dosyaları, ikili dosyalar ve sıkıştırılmış dosyalar içerir.
"l"	         sembolik bağlantı	Başka bir dosyaya işaret eder.
"s"           	soket	          İşlemler arası iletişime olanak tanır.
"p"	            boru	          İşlemler arası iletişime olanak tanır.
"b"	          blok dosyası  	  Donanımla iletişim kurmak için kullanılır.
"c"	         karakter dosyası	  Donanımla iletişim kurmak için kullanılır.


________________________________________________________________________________________________________________________________________________________________________________

*İzinler

d "rwxr-xr-x" 2 root root 4096 11 Nis 2014 yeni başlayan

İzinler, belirli kullanıcıların bir dosyaya nasıl erişebileceğini gösterir. İzinler hakkında daha fazla bilgi edinmek için okumaya devam edin.





*Sabit Bağlantı Sayısı

-rw-r----- "1" syslog adm 1346 2 Ekim 22:17 auth.log

Bu sayı, bu dosyaya kaç tane sabit bağlantının işaret ettiğini gösterir





*Kullanıcı Sahibi

-rw-r----- 1 "syslog" adm 106 2 Ekim 19:57 kern.log

Kullanıcı syslogbu dosyanın sahibidir. Her dosya oluşturulduğunda, sahiplik otomatik olarak onu oluşturan kullanıcıya atanır.




*Grup Sahibi

-rw-rw-r-- 1 root    "utmp" 292584 2 Eki 19:57 lastlog

Bu dosyanın hangi gruba ait olduğunu gösterir



*Dosya Boyutu

-rw-r----- 1 syslog adm    "19573" 2 Ekim 22:57 syslog

NOT:Dizinler ve daha büyük dosyalar kilobayt olarak gösterilebilir, çünkü boyutlarını bayt olarak göstermek çok büyük bir sayı sunar




*Zaman damgası

drwxr-xr-x 2 kök kök 4096 "7 Aralık 2017" fsck

Bu, dosyanın içeriğinin en son ne zaman değiştirildiğini gösterir.





*Dosya adı

-rw-r--r-- 1 kök kök 47816 7 Aralık 2017 "bootstrap.log"

Son alan dosya veya dizinin adını içerir.


___________________________________________________________________________________________________________________________________________________________________________________

* "-t" seçenek dosyaları zaman damgasına göre sıralayacaktır:

sysadmin@localhost : ~ $ ls -lt /var/log                                           
toplam 844                                                                       
-rw-r----- 1 syslog adm 19573 2 Ekim 22:57 syslog                             
-rw-r----- 1 syslog adm 1346 2 Ekim 22:17 auth.log                           
-rw-r----- 1 syslog adm 547 2 Ekim 22:17 cron.log                           
-rw-rw-r-- 1 root utmp 292584 2 Eki 19:57 lastlog                            
-rw-rw-r-- 1 kök utmp 384 2 Ekim 19:57 wtmp                               
-rw-r----- 1 syslog adm 106 2 Ekim 19:57 kern.log                           
-rw-r--r-- 1 kök kök 18047 20 Aralık 2017 alternatifler.log                   
-rw-r--r-- 1 kök kök 32064 20 Aralık 2017 başarısız günlüğü                            
-rw-r----- 1 kök yönetici 85083 20 Aralık 2017 dmesg                              
-rw-r--r-- 1 kök kök 325238 20 Aralık 2017 dpkg.log                           
drwxr-x--- 2 root adm 4096 20 Aralık 2017 apache2                             
drwxr-xr-x 1 root root 4096 20 Aralık 2017 apt                                
-rw-r--r-- 1 kök kök 47816 7 Aralık 2017 bootstrap.log                      
drwxr-xr-x 2 kök kök 4096 7 Aralık 2017 fsck                               
-rw-rw---- 1 kök utmp 0 7 Aralık 2017 btmp                               
drwxr-xr-x 2 root root 4096 11 Nis 2014 yeni başlayan   


____________________________________________________________________________________________________________________________________________________________________________


* "-S" seçenek dosyaları dosya boyutuna göre sıralayacaktır:

sysadmin@localhost : ~ $ ls -l -S /var/log                                         
toplam 844                                                                       
-rw-r--r-- 1 kök kök 325238 20 Aralık 2017 dpkg.log                           
-rw-rw-r-- 1 root utmp 292584 2 Eki 19:57 lastlog                            
-rw-r----- 1 kök yönetici 85083 20 Aralık 2017 dmesg                              
-rw-r--r-- 1 kök kök 47816 7 Aralık 2017 bootstrap.log                      
-rw-r--r-- 1 kök kök 32064 20 Aralık 2017 başarısız günlüğü                            
-rw-r----- 1 syslog adm 19573 2 Ekim 22:57 syslog                             
-rw-r--r-- 1 kök kök 18047 20 Aralık 2017 alternatifler.log                   
drwxr-x--- 2 root adm 4096 20 Aralık 2017 apache2                             
drwxr-xr-x 1 root root 4096 20 Aralık 2017 apt                                 
drwxr-xr-x 2 root root 4096 7 Aralık 2017 fsck                                
drwxr-xr-x 2 root root 4096 11 Nisan 2014 upstart                            
-rw-r----- 1 syslog adm 1346 2 Ekim 22:17 auth.log                           
-rw-r----- 1 syslog adm 547 2 Ekim 22:17 cron.log                           
-rw-rw-r-- 1 kök utmp 384 2 Ekim 19:57 wtmp                               
-rw-r----- 1 syslog adm 106 2 Ekim 19:57 kern.log                           
-rw-rw---- 1 kök utmp 0 7 Aralık 2017 btmp



_________________________________________________________________________________________________________________________________________________________________


*Seçenek -rherhangi bir sıralama türünün sırasını tersine çevirecektir. Önceki örneğe eklendiğinde farkı fark edin:

sysadmin@localhost : ~ $ ls -lSr /var/log
toplam 844                                                                       
-rw-rw---- 1 kök utmp 0 7 Aralık 2017 btmp                               
-rw-r----- 1 syslog adm 106 2 Ekim 19:57 kern.log                           
-rw-rw-r-- 1 kök utmp 384 2 Ekim 19:57 wtmp                               
-rw-r----- 1 syslog adm 654 2 Ekim 23:17 cron.log                           
-rw-r----- 1 syslog adm 1669 2 Ekim 23:17 auth.log                           
drwxr-xr-x 2 root root 4096 11 Nis 2014 yeni başlayan                             
drwxr-xr-x 2 root root 4096 7 Ara 2017 fsck                                
drwxr-xr-x 1 root root 4096 20 Ara 2017 apt                                 
drwxr-x--- 2 root adm 4096 20 Ara 2017 apache2                            
-rw-r--r-- 1 kök kök 18047 20 Aralık 2017 alternatifler.log                   
-rw-r----- 1 syslog adm 19680 2 Ekim 23:17 syslog                             
-rw-r--r-- 1 kök kök 32064 20 Aralık 2017 başarısız günlüğü                            
-rw-r--r-- 1 kök kök 47816 7 Aralık 2017 bootstrap.log                      
-rw-r----- 1 kök yönetici 85083 20 Aralık 2017 dmesg                              
-rw-rw-r-- 1 root utmp 292584 2 Eki 19:57 lastlog                            
-rw-r--r-- 1 kök kök 325238 20 Aralık 2017 dpkg.log 


Dosya boyutu alanındaki sayılar azalan düzenden artan düzene geçer.


__________________________________________________________________________________________________________________________________________________________________________________


*Komut su, geçici olarak farklı bir kullanıcı gibi davranmanıza olanak tanır.

*Varsayılan olarak, bir kullanıcı hesabı belirtilmezse, sukomut yönetici ayrıcalıkları sağlayan kök kullanıcı olarak yeni bir kabuk açar.

*Oturum açma kabuğu seçeneğinin kullanılması önerilir, çünkü oturum açma kabuğu yeni kabuğu yeni kullanıcının ayarlarıyla tamamen yapılandırır. Bu seçenek üç yoldan biriyle belirtilebilir:

su -
su -l
su --login 

*Girdiğimiz oturumu kapatmak için "exit" komutunu kullanırız

_____________________________________________________________________________________________________________________________________________________________________________________________

*Komut sudo, bir kullanıcının yeni bir kabuk oluşturmadan başka bir kullanıcı olarak bir komutu yürütmesine izin verir.

* "su" komutu gibi "sudo" komutu root gibi komut vermemizi sağlar.


*Komut "sudo" diğer kullanıcı hesaplarına geçmek için de kullanılabilir. Farklı bir kullanıcı hesabı belirtmek için "-u" seçeneğini kullanın.



* "ls -l" ile verileri izinleriyle birlikte getirtiriz




_______________________________________________________________________________________________________________________________________________________________________


*Dosya Türü Alanı

"-" rw-r--r-- 1 sysadmin sysadmin 647 20 Aralık 2017 hello.sh
 
Bu çıktının ilk karakteri bir dosyanın türünü belirtir. İlk karakterin bir ise "-", bunun normal bir dosya olduğunu hatırlayın. Karakter bir ise "d", bu bir dizin olurdu.


*İzin Alanı
- "rw-r--r--" 1 sysadmin sysadmin 647 20 Aralık 2017 hello.sh

Dosya türü karakterinden sonra izinler görüntülenir. İzinler üç karakterden oluşan üç sete ayrılır:

*Mal sahibi
*Grup
*Diğer



*Mal sahibi

- "rw"- r--r-- 1 sysadmin sysadmin 647 20 Aralık 2017 hello.sh
 
*İlk set dosyanın sahibi olan kullanıcı içindir. Mevcut hesabınız dosyanın kullanıcı sahibiyse, üç izin setinin ilki geçerli olur ve diğer izinlerin hiçbir etkisi olmaz.

*Dosyanın sahibi olan kullanıcı ve bu izinlerin kimlere uygulanacağı, kullanıcı sahibi alanıyla belirlenebilir :

-rw-r--r-- 1 "sistem yöneticisi" sistem yöneticisi 647 20 Aralık 2017 hello.sh





*Grup


-rw- "r--" r-- 1 sysadmin sysadmin 647 20 Aralık 2017 hello.sh

*İkinci set dosyanın sahibi olan grup içindir. Mevcut hesabınız dosyanın kullanıcı sahibi değilse ve dosyanın sahibi olan grubun üyesiyseniz, grup izinleri geçerli olur ve diğer izinlerin hiçbir etkisi olmaz .

*Bu dosyanın grubu , grup sahibi alanıyla belirlenebilir :

-rw-r--r-- 1 sistem yöneticisi "sistem yöneticisi" 647 20 Aralık 2017 hello.sh




*Diğer


-rw-r-- "r--" 1 sistem yöneticisi sistem yöneticisi 647 20 Aralık 2017 merhaba.sh

*Son set, ilk iki izin setinin uygulanmadığı herkes içindir. Dosyanın sahibi olan kullanıcı veya dosyanın sahibi olan grubun üyesi değilseniz, üçüncü izin seti sizin için geçerlidir.

______________________________________________________________________________________________________________________________________________________________________________________________

İzin          	Dosya Üzerindeki Etkiler                                           	Dizin Üzerindeki Etkiler

Okumak ( r)  	Dosya içeriğinin okunmasına veya kopyalanmasına izin verir.         	Dizin üzerinde yürütme izni olmadan, dosyaların ayrıntılı olmayan bir listesini sağlar. Yürütme izniyle, ls -layrıntılı bir 
                                                                                    listeleme sağlanabilir.
yazmak ( w)	  İçeriklerin değiştirilmesine veya üzerine yazılmasına izin verir.     Dosyaların bir dizine eklenmesine veya dizinden kaldırılmasına izin verir.	Bu iznin çalışabilmesi için dizinin aynı zamanda 
                                                                                    yürütme iznine de sahip olması gerekir.
uygulamak ( x)	Bir dosyanın bir işlem olarak çalıştırılmasına izin verir,
                ancak komut dosyalarının okuma iznine de ihtiyacı vardır.          	Üst dizinlerde de yürütme izni varsa, kullanıcının dizine geçmesine izin verir.




***
Hangi izinlerin geçerli olduğunu anlamak Linux'ta önemli bir beceri setidir. Örneğin, aşağıdaki izin setini düşünün:

 -r--rw-rwx. 1 sysadmin staff 999 Apr  10  2013 /home/sysadmin/test

 

Verilen izin seti:
-r--rw-rwx

Bu izinleri parçalara ayırırsak:

- → Bu bir dosya (d olsaydı, bir dizin olurdu).
r-- → Sahip (sysadmin) sadece okuma iznine sahip.
rw- → Grup (staff) okuma ve yazma izinlerine sahip.
rwx → Diğer herkes okuma, yazma ve çalıştırma izinlerine sahip.
Buradaki önemli nokta:

Kullanıcı sysadmin, dosyanın sahibi olduğu için yalnızca sahip izinleri geçerli olur.
Yani sysadmin, grubun (staff) veya diğer herkesin (rwx) sahip olduğu ek izinleri kullanamaz.
Sahip için sadece r-- (okuma) izni olduğundan, sysadmin dosyayı açıp içeriğini görebilir, ancak değiştiremez veya çalıştıramaz.
Eğer sysadmin bir grup üyesi olsaydı bile, sahiplik izinleri öncelikli olduğu için yine de sadece okuma iznine sahip olurdu.



__________________________________________________________________________________________________________________________________________________________________________________________________













