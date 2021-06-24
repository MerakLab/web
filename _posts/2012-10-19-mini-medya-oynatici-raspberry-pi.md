---
id: 648
title: 'Mini Medya Oynatıcı: Raspberry Pi'
date: 2012-10-19T16:16:56+03:00
author: Murat Eray KORKMAZ
layout: post
guid: http://www.murateray.com/?p=648
permalink: /mini-medya-oynatici-raspberry-pi/
Views:
  - "693"
wpb_post_views_count:
  - "6188"
custom_sidebar:
  - ""
saturn_post_views:
  - "85"
image: /wp-content/uploads/2012/10/kapak_rpi.jpg
categories:
  - Bilgisayar
tags:
  - htpc
  - media player
  - medya oynatıcı
  - raspberry pi
  - raspbian
  - xbian
  - xmbc
---
Minik dev Raspberry Pi.

Raspberry Pi&#8217;yi ilk olarak 2011&#8217;in sonlarına doğru Donanım Haber&#8217;de çıkan [bir haberle](http://www.donanimhaber.com/hazir-pc/haberleri/25-dolarlik-bilgisayar-Raspberry-Pi-uretime-giriyor.htm) duymuştum. 25$&#8217;lık bir bilgisayardan söz ediyordu. Fiyatı ucuz olunca ne işe yarar acaba diye sorgulamadan &#8220;Bir tane edilmeliyim.&#8221; diye içimden geçirdim ve geçirdiğimle kaldım. Bu haberden yaklaşık 2-3 ay kadar sonra Mart 2012&#8217;de bu sefer ShiftDelete.Net&#8217;ten [tükendiğinin haberini](http://shiftdelete.net/raspberry-pi-dakikalar-icinde-tukendi-35331.html) okudum. Haberin sonunda &#8220;Yakın bir zamanda yeniden piyasaya sürülmesi bekleniyor.&#8221; ibaresini görünce bu sefer işi şansa bırakmamaya karar verdim ve kısa bir araştırmayla [Farnell](http://farnell.com)&#8216;i buldum.

<!--more-->

Farnell&#8217;in desteklediği [element14](http://www.element14.com/community/groups/raspberry-pi), Raspberyy Pi&#8217;nin dağıtımcılarından biri. Ürünün tükendiğini öğrendikten sonra sitenin posta grubuna üye olup, yeni modelin piyasaya sürülmesini beklemeye koyuldum. Nisan&#8217;ın ortalarında ön siparişlerin başladığının haberi geldi ve hemen siparişi verdim. Ağustos ayının başlarında üretimin tamamlandığının dağıtımının başladığına dair bir bilgiyle beraber kredi kartından ücreti çekemediklerine dair bir mesaj aldım. Ön sipariş için kayıt olurken verdiğim kartın süresi dolduğundan iptal olmuştu. Yeni kart numarası ile siparişim güncelledim ve 15 gün sonra, Ağustos ortasında paket kapıma geldi. _Şu an ön sipariş sayfası açık, ilgilenenler [şuradan](http://downloads.element14.com/raspberryPi1.html?COM=raspi-group) ön sipariş verip 3-4 hafta içinde cihazlarına kavuşabilirler._

<img loading="lazy" class="aligncenter size-full wp-image-1670" src="https://i0.wp.com/www.murateray.com/wp-content/uploads/2012/10/0_paket.jpg?resize=740%2C492" alt="Kargo Paketi" width="740" height="492" data-recalc-dims="1" /> 

Raspberry Pi ilk olarak 2006 yıllarında küçük ve ucuz bilgisayar üretme fikri olarak ortaya çıkmış ve üzerinde çalışılmaya başlanmış. 2011 Ağustos&#8217;unda 50 adet test cihazı üretilip test edilmiş. Şubat 2012&#8217;de ise ilk seri üretim cihazlar satışa çıkmış ve çıktığı an tükenmiş. Sonrasında ise Nisan ayında bu sefer ön siparişle satışa açıldı ve fırsat bu fırsat ben de bir tane kaptım. Eylül ayı itibariyle yaklaşık 500bin cihazın satıldığı [söylenmekte](http://www.wired.com/opinion/2012/09/raspberry-pi-insider-exclusive-sellout-to-sell-out/).

<img loading="lazy" class="aligncenter size-full wp-image-1672" src="https://i1.wp.com/www.murateray.com/wp-content/uploads/2012/10/2_kutu.jpg?resize=740%2C492" alt="Ürün Kutusu" width="740" height="492" data-recalc-dims="1" /> 

[Raspberry Pi](http://www.raspberrypi.org), dünyanın en ucuz Linux tabanlı bilgisayarı olarak 25$ ve 35$&#8217;lık iki modeli ile birlikte piyasa sunuldu. İki model arasındaki en belirgin farklı 35$&#8217;lık B modelinde 256 MB yerine 512 MB&#8217;lık RAM, ikinci bir USB portu ve ek olarak 10/100&#8217;lük ethernet portu vardı. Benim edindiğim 35$&#8217;lık B modeli idi.

<img loading="lazy" class="aligncenter size-full wp-image-1673" src="https://i2.wp.com/www.murateray.com/wp-content/uploads/2012/10/3_kutu.jpg?resize=740%2C492" alt="Kutu Detayları" width="740" height="492" data-recalc-dims="1" /> 

Raspberry Pi, gerçekten ufacık bir bilgisayar. Kutusu, sigara paketi büyüklüğünde. Cihazın kendisi de 86&#215;54 mm boyutları ile bir avuca sığabilecek büyüklükte ve 45 gr neredeyse hissedilmeyecek kadar hafiflikte.

<img loading="lazy" class="aligncenter size-full wp-image-1674" src="https://i0.wp.com/www.murateray.com/wp-content/uploads/2012/10/4_raspberrypi.jpg?resize=740%2C492" alt="Raspberry Pi" width="740" height="492" data-recalc-dims="1" /> 

Buna rağmen koca masaüstü bilgisayarlarda veya bir parça daha küçük dizüstü bilgisayarlarda bulunan hemen hemen her şey ve hatta daha fazlasını bünyesinde barındırmakta.

Cihaz üzerinde Broadmcom BCM2835 çipi bulunuyor. Çip, bünyesinde CPU, GUP, DSP, SDRAM ve USB portunu barındırmakta. İşlemci olarak 700 MHz&#8217;lik ARM işlemcisi kullanılmakta. 512 MB RAM ise grafik işlemciyle de paylaşılmakta. Grafik işlemci olarak yine Broadcom&#8217;un VideoCore IV GPU&#8217;su kullanılmakta. Tüm bu donanım h.264-MPEG-4 codecleri çözüp &#8211;_benim önceliğim olduğu için ilk bu konuda test yaptım_&#8211; FullHD videoları kesintisiz oynatabilecek güce sahip.

<img loading="lazy" class="aligncenter size-full wp-image-1675" src="https://i1.wp.com/www.murateray.com/wp-content/uploads/2012/10/12_raspi.jpg?resize=740%2C492" alt="Raspberry Pi Üstten Görünüş" width="740" height="492" data-recalc-dims="1" /> 

Monitöre ve/veya LCD/LED TV&#8217;ye bağlantı için [HDMI](http://tr.wikipedia.org/wiki/HDMI) 1.4 arabirimi mevcut. Bu arabirim ile hem görüntüyü hem de sesi sorunsuzca ve basitçe ekrana aktarabilmek mümkün. 1920&#215;1080 yani FullHD çözünürlüğü desteklemekte ve çalışırken herhangi bir sıkıntı çıkarmamakta.

<img loading="lazy" class="aligncenter size-full wp-image-1676" src="https://i1.wp.com/www.murateray.com/wp-content/uploads/2012/10/6_hdmi.jpg?resize=740%2C492" alt="Raspberry Pi HDMI Girişi" width="740" height="492" data-recalc-dims="1" /> 

HDMI portunu kullanmak istemeyenler için de analog ses ve görüntü çıkışları da mevcut elbette. HDMI dışında sesi [3.5 mm jack](http://tr.wikipedia.org/wiki/TRS_konnektörü) aracılığıyla dışarıya verebilmek mümkün. Görüntüyü ise yine [kompozit video](http://tr.wikipedia.org/wiki/Kompozit_Video) çıkışını kullanarak aktarmak mümkün. Tercih meselesi tabi ama imkan varsa HDMI görüntü/ses aktarımını kolayca ve hızlıca gerçekleştirebiliyor.

<img loading="lazy" class="aligncenter size-full wp-image-1677" src="https://i0.wp.com/www.murateray.com/wp-content/uploads/2012/10/7_audiovideo.jpg?resize=740%2C492" alt="Raspberry Pi Audio Analog Video Girişi" width="740" height="492" data-recalc-dims="1" /> 

İnternet bağlantısı içinse iki modeli birbirinden ayıran ve B modelinde yer alan özelliklerden biri olan [10/100 Ethernet](http://tr.wikipedia.org/wiki/Ethernet) portu mevcut. Bu sayede [RJ45 kablo](http://tr.wikipedia.org/wiki/RJ45) ile Raspberry Pi&#8217;yi internete bağlayabilirsiniz. Ayrıca sahip olduğu USB portları aracılığıyla bağlayacağınız Wi-Fi adaptörlerle kablosuz olarak da internet bağlantısı kurabilmeniz mümkün. Raspberry Pi üzerinde 2 adet USB 2.0 port bulunmakta. Bu portlar az görünmesine rağmen bağlayacağınız herhangi bir [USB Hub](http://tr.wikipedia.org/wiki/USB_hub) ile portlarınızı aktarabilmenin mümkün. Böylece klavye/mouse mu bağlasam, wi-fi adaptör mü bağlasam yoksa taşınabilir disklerimi mi -veya hangisini- bağlasam diye düşünmek zorunda kalmazsınız.

<img loading="lazy" class="aligncenter size-full wp-image-1678" src="https://i1.wp.com/www.murateray.com/wp-content/uploads/2012/10/8_ethusb.jpg?resize=740%2C492" alt="Raspberry Pi Ethernet USB Girişi" width="740" height="492" data-recalc-dims="1" /> 

Cihaz, güç kaynağı olarak 5 volta ihtiyaç duyuyor ve bu ihtiyacını [MicroUSB](http://en.wikipedia.org/wiki/MicroUSB#Mini_and_Micro_connectors) kablo ile sağlayabiliyor. Kablo/adaptör alırken iki şeye dikkat etmek lazım. Birincisi kablo ucunun Mini USB değil Micro USB olmasına dikkat edilmeli. İkicinsi de adaptörün Raspberry Pi&#8217;nin ihtiyaç duyduğu 700 mA (3.5W) gücü karşılayabilmesi lazım. Ben adaptör ararken daha düşün güç üreten modellerinin olduğunu da gördüm. Biraz daha yüksek güç sağlayan bir adaptör almakta fayda var zira duyduğum kadarıyla -ve kitapçıkta yazdığına göre- düşük güç ürtenler çalışma performansına etki edebiliyormuş. Özellikle USB Hub bağlanması veya cihazın tüm portlarından bilgi alış-verişi olması durumunda güç yetersiz gelebiliyor.

<img loading="lazy" class="aligncenter size-full wp-image-1679" src="https://i0.wp.com/www.murateray.com/wp-content/uploads/2012/10/10_power.jpg?resize=740%2C492" alt="Raspberry Pi MicroUSB Girişi" width="740" height="492" data-recalc-dims="1" /> 

<img loading="lazy" class="aligncenter size-full wp-image-1680" src="https://i2.wp.com/www.murateray.com/wp-content/uploads/2012/10/15_powercord.jpg?resize=740%2C492" alt="Raspberry Pi Güç Kablosu MicroUSB" width="740" height="492" data-recalc-dims="1" /> 

Son olarak da cihazın diskine değinmek lazım. Cihazın bu kadar küçük ve de ucuz olmasının altında yatan sebeplerden biri de bünyesinde dahili bir disk barındırmıyor olmasıdır. Cihaz üzerinde SD/MMC kart takılabilecek bir yuva bulunmakta ve kapasite sınırlaması, kullandığınız kart büyüklüğü ile ilgili oluyor.

<img loading="lazy" class="aligncenter size-full wp-image-1681" src="https://i0.wp.com/www.murateray.com/wp-content/uploads/2012/10/11_sd.jpg?resize=740%2C492" alt="Raspberry Pi SD Kart Girişi" width="740" height="492" data-recalc-dims="1" /> 

Ben elimdeki Kodak SDHC 8 GB Class 2 kartı kullanıyorum. Class 2, SD kartlar içerisinde [veri aktarım hızı en düşük](http://tr.wikipedia.org/wiki/SD_kart#Transfer_H.C4.B1z.C4.B1) olan kart. Yaklaşık olarak 2 MB/s&#8217;lik bir veri aktarım hızı var. Buna rağmen örneğin denediğim 1080p videoyu kesintisiz olarak seyredebildim. Daha yüksek hızlı kartlar özellikle sistemin genel çalışmasında mutlaka etkiye sahip olacaktır. Ancak benim gibi medya oynatıcı olarak kullanacaksanız yüksek hızlara ihtiyaç duymayacaksınızdır. Yine de günümüzde fiyatları birbirine çok yaklaştığını düşünürsek alınacak daha hızlı kartlar, performansı arttıracaktır.

<img loading="lazy" class="aligncenter size-full wp-image-1682" src="https://i2.wp.com/www.murateray.com/wp-content/uploads/2012/10/13_hdd.jpg?resize=740%2C492" alt="Raspberry Pi SD Kart" width="740" height="492" data-recalc-dims="1" /> 

SD kart kullanımın bence şöyle bir avantajı mevcut, en azından kendi adıma. İlk etapta kullanım amacım hobi olarak ve medya oynatıcı olarak kullanmaktı. Bunun yanında, vakit dahilinde uğraşınca çok güzel projelere altyapı olabiliyor. Şu an hali hazırda çeşitli dağıtımlara ulaşabilmek mümkün. Raspberry Pi tarafından desteklenen, Debian tabanlı [Raspian](http://www.raspbian.org) ve ArchLinux tabanlı [Archlinux|ARM](http://archlinuxarm.org/platforms/armv6/raspberry-pi) işletim sistemlerini başlı başına bir bilgisayar olarak kullanabileceğiniz gibi sadece medya oynatıcı olarak kullanabileceğiniz ve açıldığı an direkt olarak karşınıza medya oynatıcı arabirimi gelen ve ikisi de [XMBC](http://xbmc.org) tabanlı olan [RaspBMC](http://www.raspbmc.com) ve [XBian](http://xbian.org) sistemleri de mevcut. Gerek Raspberry Pi gerekse de yazılım tarafındaki sistemler daha çok yeni ve hala geliştirilme aşamasında. Günden güne performansları ve stabiliteleri düzeltilmektedir. Bu yüzden gelişmeleri hızlıca takip etmek ve kalıcı olarak kullanacağınız sistemi tercih etmek için biraz zaman harcayıp hepsini denemekte fayda var. Bu noktada da SD kart kullanımı hem pratik hem de ekonomik bir çözüm oluyor. Hatta 2-4 GB&#8217;lık kartlar o kadar ucuz ki 2-3 tane edinilip her birine bu sistemlerden biri yükleyip el altında tutulabilir.

Ben bir süredir XBian&#8217;ı kullanmaktayım. Raspberry Pi&#8217;yi HDMI kablo ile [Sony KDL-40EX520 FullHD LED TV](http://www.sony.com.tr/product/tv-102-40-lcd/kdl-40ex520)&#8216;ye bağladım. Maalesef Sony, dahili USB portları ile özellikle mkv formatını çalıştırmadığından harici medya player şarttı. Bu açığı da en ucuz -ve bence en verimli şekilde- Raspberry Pi ile kapatmaya karar verip, siparişimi vermiştim. Pişman da değilim.

<img loading="lazy" class="aligncenter size-full wp-image-1683" src="https://i1.wp.com/www.murateray.com/wp-content/uploads/2012/10/16_set.jpg?resize=740%2C492" alt="Raspberry Pi Düzenek" width="740" height="492" data-recalc-dims="1" /> 

Kısaca baktığımızda, ses ve görüntü aktarımını HDMI ile yaptım. Ethernet ile internete bağladım. Arabirimi kontrol için bir adet klavye taktım. Diğer USB portuna ise [Western Digital MyBook 2 TB](http://www.wdc.com/en/products/products.aspx?id=870) harici diskini bağladım. Disk NTFS ile formatlanmıştı ve herhangi bir problem yaşamadım. Disk olarak da yukarıda belirttiğim gibi Kodak 8 GB SD Class 2 kartını kullandım. Benim için önemli olan nokta medya oynatıcı özelliği olduğundan dolayı ilk testim h264 codec ile sıkıştırılmış FullHD filmleri barındıran mkv dosyalarındaki performansı idi. Beklediğimden çok daha iyi sonuç verdi ve kesintisiz olarak oynattı. Görüntü başarılıydı keza aynı şekilde ses de öyle. Arabirimi kullanmak için bir adet de klavye bağlamıştım. Şans eseri elim kumandaya çarpınca farkettim ki HDMI ile bağladığımız takdirde tüm fonksiyonları kumanda üzerinden kullanabiliyoruz. Menüler içinde gezinme, film seçimi, filmi başlatma/durdurma/ileri-geri sarma vs her işlem yapılabiliyor. Böylece klavyeyi de çıkardım ve zaten küçük olan cihazı televizyonun arkasına güzelce gizledim. İnternette çok güzel/ucuz kutular [bulabilmek](http://www.google.com.tr/#hl=en&output=search&sclient=psy-ab&q=raspberry+pi+case&oq=raspberry+pi+case&gs_l=hp.3...580.2469.0.2637.17.13.0.1.1.3.613.2596.0j2j2j3j0j1.8.0...0.0...1c.1.9bg_7HJxnGQ&pbx=1&bav=on.2,or.r_gc.r_pw.r_cp.r_qf.&fp=2825acac8a3daa27&bpcl=35466521&biw=1280&bih=611) mümkün aynı şekilde [ebay](http://www.ebay.com/sch/i.html?_trksid=p5197.m570.l1313&_nkw=raspberry+pi+case&_sacat=0&_from=R40)&#8216;de de farklı bir sürü ürün mevcut. Mesela cihazın güzelliğini de sergileyen [şu kutu](http://www.ebay.com/itm/New-Raspberry-Pi-Closed-Case-from-Rascase-/251123638323?pt=US_Computer_Cases&hash=item3a7822a033) oldukça güzel/ucuz. Özellikle [ModMyPi](https://www.modmypi.com/shop/)&#8216;de hem çeşitli kutular hem de çeşitli Raspberry Pi ürünleri mevcut, göz atmakta fayda var.

Toparlamak gerekirse,

  * Teknolojiyle ilgilenenler için çok güzel/keyifli bir cihaz olduğunu düşünüyorum. Ürünü ilk duyduğumda -hani kullanmasam bile- alayım, biraz kurcalarım dursun bir kenarda bile dedim.
  * Cihaz gerçekten çok ufak, gerçekten çok ucuz. Buna rağmen yapabildikleri gerçekten çok fazla. Ben burada sürekli medya oynatıcı olarak kullanmaktan bahsettim, bu buz dağının sadece ucu. Medya oynatıcı veya gerçek bir bilgisayar olarak kullanmak dışında proje bazlı olarak kullanım alanı uçsuz bucaksız. Çok basit, kendin yap projelerinde kullanılabileceği gibi ticari/akademik düzeyde yapılacak çalışmalarda da kesinlikle kullanılabilir bir cihaz. Bununla ilgili ufak bir araştırma yapıldığında zaten onlarca proje ile karşılaşmak mümkün. Mesela bana ilginç gelen projelerden biri üzerinde [Android çalıştırılması](http://www.diyphonegadgets.com/2012/07/raspberry-pi-runs-android-for-first.html) ile ilgili. Benzer şekilde Firefox OS için de bir [çalışma mevcut](http://www.raspberrypi.org/archives/1787).
  * Bahsettiğim gibi cihaz ucuz. 35$&#8217;a sipariş veriyorsunuz ve kargo dahil yaklaşık 80 TL&#8217;ye kapınıza kadar geliyor. Yaptığı işin yarısını yapan en ucuz/özelliksiz medya oynatıcılar bile 100 TL&#8217;den çok daha yüksek ücretlere satılıyor.
  * Ürün çok yeni. Yabancı kaynaklar ve cihazla yapılabilecekler -şu an için- sınırlı. Türkçe kaynak yok denecek kadar az. Konuyla ilgilenenler için [Raspberry Pi Türkiye Topluluğu](http://www.raspberrypi.gen.tr) önemli ve güzel bir Türkçe kaynak. Yabancı kaynaklardan ise [şurada](http://www.raspberrypi-tutorials.co.uk), [şurada](http://www.rpiforum.net/forum/) ve Cambridge Üniversitesi&#8217;nin de [şurada](http://www.cl.cam.ac.uk/freshers/raspberrypi/tutorials/) yer alan kaynağında güzel bilgiler mevcut. Keza Cambridge&#8217;in sitesinde Raspberry Pi&#8217;ye özel işletim sistemi geliştirlmesini anlatan [güzel bir seri](http://www.cl.cam.ac.uk/freshers/raspberrypi/tutorials/os/) de mevcut.Google araştırma için yeterli bir kaynak. Gerisi hayal gücünüze ve yapmak istediklerinize kalıyor. Ayrıca Raspberry Pi ile ilgili [güzel kitaplara](http://www.amazon.co.uk/s/ref=nb_sb_noss?url=search-alias%3Dstripbooks&field-keywords=raspberry+pi) da Amazon üzerinden erişebilmek mümkün.
  * Medya oynatıcı olarak hep iyi taraflarından bahsettim. İleri-geri sarmalarda ufak takılmalar mevcut, eklemeden geçmeyeyim. Görüntüyü sardıktan sonra 2-3 saniye içinde görüntü düzeliyor. Kendi adıma kabul edilebilir buluyorum.
  * Henüz Raspbian vb. sistemleri kullanmadığımdan masaüstü performansı konusunda net bir şey şimdilik söyleyemiyorum. Zaman için daha detaylı incelemeler yapıp bunlarla ilgili de bir şeyler paylaşmayı düşünüyorum.
  * Cihaz çok yeni olduğundan, yazılım tarafında da geliştirmeler sürekli/hızlı olduğundan akşamından sabahına yeni güncelleştirmeler çıkabiliyor. Özellikle performans ve stabilite anlamında çok fayda sağlıyorlar, takip etmekte ve cihazı/yazılımı belli aralıklarla güncellemekte fayda var.

Son olarak da cihazla ilgili ufak bir unboxing videosu paylaşmadan geçmeyeyim. Bunu da kısa bir tanıtım olarak düşünmek mümkün. İlerleyen günlerde kurulum ve kullanımı ile ilgili olarak da paylaşacaklarım var.

<span class="embed-youtube" style="text-align:center; display: block;"></span> 

Burada da parçaların bir araya ve kullanıma hazır hale getirdiğim ufak bir video var.

<span class="embed-youtube" style="text-align:center; display: block;"></span> 

Umarım faydalı bir yazı olmuştur. Konuyla ilgili olarak sormak istedikleriniz olursa, elimden geldiğince yardımcı olmaya çalışırım. İlk fırsatta işletim sistemi/yazılımın kurulumu ve kullanımı ile ilgili de bir yazı ve kısa video hazırlamaya çalışacağım. Yazıyı bekleyemeyecek kadar sabırsız olanlar için [şurada](http://www.howtogeek.com/119924/build-a-35-media-center-with-raspbmc-and-raspberry-pi/) &#8211;_maalesef İngilizce_&#8211; güzel bir anlatım mevcut, göz atabilirsiniz.