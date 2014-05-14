XOR-YapaySinirAg
================

XOR-YapaySinirAg
 
                            			Yapay Sinir Ağları – XOR Örneği (C#)

Yapay sinir ağları (YSA), insan beyninin bilgi işleme tekniğinden esinlenerek geliştirilmiş bir bilgiişlem teknolojisidir. YSA ile basit biyolojiksinir sisteminin çalışma şekli simüle edilir (benzetilir). Simüle edilen sinir hücreleri nöronlariçerirler ve bu nöronlar çeşitli şekillerde birbirlerine bağlanarak ağı oluştururlar. Bu ağlar öğrenme, hafızaya alma ve veriler arasındaki ilişkiyi ortaya çıkarma kapasitesine sahiptirler. Diğer bir ifadeyle, YSA’lar, normalde bir insanın düşünme ve gözlemlemeye yönelik doğal yeteneklerini gerektiren problemlere çözüm üretmektedir. Bir insanın, düşünme ve gözlemleme yeteneklerini gerektiren problemlere yönelik çözümler üretebilmesinin temel sebebi ise insan beyninin ve dolayısıyla insanın sahip olduğu yaşayarak veya deneyerek öğrenme yeteneğidir.( wikipedia)

Adaline

1959’da, Stanford Üniversitesinden Bernard Widrow, basit nöron benzeri elemanlara dayanan ve “Adaline” (Adaptive Linear Nöron) olarak adlandırılan bir adaptif lineer elemanı geliştirmiştir. Adaline yapısı tüm sinir ağlarının en basitidir ve öğrenme için danışmanlı öğrenmeyi kullanır. Adaline ve iki tabakalı biçimi olan “madaline” (Multiple Adaline); ses tanıma, karakter tanıma, hava tahmini ve adaptif kontrol gibi çok çeşitli uygulamalar için kullanılmıştır. Daha sonraları adaline, ayrık bir çıkış yerine sürekli bir çıkış üretmek için geliştirilmiştir. Widrow, telefon hatları üzerindeki ekoları elimine etmeye yarayan adaptif filtreleri geliştirmede, adaptif lineer eleman algoritmasını kullanmıştır. Bununla ilk defa YSA’lar gerçek bir probleme uygulanmıştır. Adaline bir çok uygulama için oldukça iyi çalışmasına rağmen lineer problem uzayıyla sınırlıdır. Lineer transfer fonksiyonu kullanırlar. Giriş ve istenilen çıkış desenlerinin tekrar tekrar ağa uygulanmasıyla eğitim gerçekleştirilir. Desenlerin doğru sınıflara ayrılmasıyla, hatalar minimize edilerek öğrenme gerçekleştirilir. Eğitimden sonra adaline, yeni girişleri kazandığı deneyime göre sınıflandırabilir.

Adaline Ünitesinin Öğrenme Kuralı

      Adaline ünitesinin öğrenme kuralı, YSA’lardaki geneler öğrenme prensibine göre çalışmaktadır. Girdilerden çıktılar hesaplanır ve ağırlıklar çıktıya göre değiştirilir. ADALİNE ünitesinin net girdisi Net ve çıktısı (Ç) aşağıdaki formül ile hesaplanmaktadır.

NET = ∑w i x i+f

Eğer NET >= 0 çıktı (Ç)=1
Eğer NET < 0 çıktı (Ç)=-1
Çıktı hesaplandıktan sonra, ADALİNE ünitesinin hatası aşağıdaki formül ile hesaplanır.
E=B-Ç  Olacaktır.

Amaç, bu hatayı en aza indirecek ağırlıkları bulmaktır. Bunun için ağa her seferinde farklı örnekler gösterilerek hatalar hesaplanmakta ve ağırlıklar hatayı azaltacak şekilde değiştirilmektedir. Zaman içinde hata, olması gereken en küçük değere düşmektedir. Bu hatayı azaltmak için kullanılan kural şu formül ile gösterilmektedir.

 

Wy = We + a*E*Xi
Her hangi bir t a anında,
Wi (t) = Wi (t-1) + a * E* Xi olacaktır.

Wi (t) : Ağırlıkların t zamanındaki değerleri
Wi (t-1) : Ağırlıkların t zamanındaki değerleri
a : Öğrenme katsayısı
B: Beklenen Çıktı
E: Beklenen değer ile çıktı arasındaki hata
X: Girdiler

Benzer şekilde, eşik değerinin zaman içindeki değeri de

fy= fe + a (B-Ç)

formülü ile hesaplanır.

işlem Adımları

-0.5 ile 0.5 arasında ağırlık değerlerinin rastgele atanması(Biz kendimiz belirliyoruz);
Hedef çıktı ve girdi değerlerinin seçimi,
Hata oranının hesaplanması,
Ağırlıkların düzenlenmesi,
Hata değeri sıfır olana kadar işlemin devamı,
Yeni girdilerin verilecek işlemin devam
