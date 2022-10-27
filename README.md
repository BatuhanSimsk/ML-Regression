# ML-Regression

Makine Öğrenimi, denetimli öğrenme ve denetimsiz öğrenme olarak ikiye ayrılır.
Denetimsiz öğrenmenin bir alt başlığı kümeleme, denetimli öğrenmenin alt başlıkları sınıflandırma ve regresyondur.
Makine öğrenmesinde eldeki veriler belirli modeller yardımıyla eğitilir, eğitim sonrasında modele verilecek olan yeni veriler üzerinden tahminler yürütmesi beklenir.
Regresyon, bağımlı değişken(ler) ile bağımsız değişken arasındaki ilişkinin matematiksel olarak modellenmesi için kullanılır. Regresyonun sonucu net sayısal veriler olmalıdır.

Basit Doğrusal Regresyon
Yalnıza bir bağımlı değişkenin bağımsız değişken üzerindeki etkisini gösteren matematiksel modellerdir.
Y=ß0+ß1X1+e

Regresyonda bağımlı değişkenlerin bağımsız değişkenler üzerindeki etkisi R2 değeri ile hesaplanır.
R2 değeri, Toplam Kareler Toplamı değerinden Artık Kareler Değerinin çıkarılması sonucunda oluşan sonucun Toplam Kareler Toplamına bölünmesi ile bulunur.
R2 0-1 arasında bir değer alır. R2 değerinin 1’e yakın olması bağımsız değişkenlerin, bağımlı değişkenleri daha iyi bir şekilde açıkladığını gösterir.



Çoklu Doğrusal Regresyon
Çoklu doğrusal regresyonda, basit doğrusal regresyonun aksine birden fazla bağımlı değişken vardır. Basit doğrusal regresyona göre daha kompleks bir yapıya sahiptir. Genel denklemi;
Y = ß0 + ß1.x1 + ß2.x2 + ... + ßk.xk+ei = ß0+ΣßrXr+e şeklindedir.

P değeri nedir?
Yapılan varsayımın doğru/tutarlı olup olmadığını istatistiksel bir ölçütüdür.
Veri setinin P değeri önceden belirlenen varsayılan değerin altındaysa, hipotez reddedilir.

Çoklu Regresyon Modeli oluşturulurken her bir değişkenin etkisi farklı olduğundan, bu durum dikkatle incelenmelidir. Kaldırılan önemli bir veri büyük bir kayba yol açabilir, ya da düşük etkiye sahip bir değişkenin kaldırılmaması istenmeyen sonuçlara yol açabilir.

Çoklu Regresyon Modeli kurulumunda genel olarak benimsenmiş 5 metod vardır.
Bunlar ;
Bağımsız değişkenlerin hepsini birden modele dahil etmek (All-in)
Geriye doğru eleme (Backward Elimination)
İleriye doğru seçme (Forward Selection):
İki yönlü eleyerek seçme (Bidirectional Elimination)
Sonuçları karşılaştırma (Score comparision) 
şeklinde ifade edilebilir.

Geriye Doğru Eleme

Geriye doğru eleme yöntemi tüm değişkenleri içeren bir modelden, fazlalıklarını atarak daha verimli daha küçük bir model oluşturma içeren algoritmadır.
Değişkenlerin modelde kalması için önem değeri belirlenir. Bir çeşit eşik  değeri(threshold) olarak işlev görür. (p<0.05)
Modelle alakasız değişkenler modelden çıkarılır.
En yüksek P değerine sahip değişkeni bul. Eğer önem değerinden yüksekse (P>SL) bir sonraki adıma ilerle. Eğer düşükse modelin geriye doğru eleme algoritmasını tamamlamıştır.
P değeri önem değerinden yüksek değişkeni modelden çıkart ve 3. adıma dön.

İleri Doğru Seçme
İleri doğru seçme yöntemi geriye doğru eliminasyon yönteminden farklı olarak hiçbir bağımsız değişken içermeyen bir model olarak başlar.
Sonrasında ise hipoteze en yararlı olduğu tahmin edilen değişkenleri alarak kendisini daha büyük bir model haline getirir. 

İşleyişi ise şöyledir:
Modele giriş için bir önem değeri belirlenir.
Bütün bağımsız değişkenler ve bağımlı değişkenle ayrı ayrı ikişerli modeller oluşturulur. En küçük P değerine sahip değişken seçilir. Seçilen değişken modele eklenir. Bundan sonrasında ise belirlenen önem değerinden düşük olmakla beraber yine en küçük P değerine sahip değişken modele eklenir.
Bu işlem seçilen yeni değişkenin P değerinin önem değerinden fazla olmasına kadar devam eder. En küçük P değerine sahip yeni değişkenin P değerinin önem değerinden fazla olduğunu gördüğümüzde daha önce eklediğimiz değişkenlerin model için yeterli olduğunu anlamalıyız.

Regresyon analizi iki veya daha fazla değişkenin istatistiki açıdan incelenmesi için kullanılan yöntemdir. Regresyon analizinin adımları aşağıdaki gibidir.

Hipotez Oluşturulur
Regresyon analizi yapmak için, ilişkili olduğu varsayılan iki değişken seçilmelidir, bu değişkenlerin ilişkileri hakkında hipotez oluşturulur.
Grafik Oluşturulur
İki veri seti ile doğrusal regresyon için temel bir çizgi grafiği oluşturulabilir. Bir değişken X diğeri ise Y ekseninde çizilir. Bir elektronik tabloya girdiğinizde, değişkenler arasındaki korelasyonu gözlemlenebilir. Düz bir çizgi varsa, bu pozitif bir korelasyon gösterir.

Sonuçlar Analiz Edilir
Grafiği temel bir doğrusal regresyonda inceleyerek kesişim, katsayı ve korelasyonu görebilirsiniz. Bu rakamları bir araya getirmek, iki veri seti arasındaki tarihsel ilişkiyi göstererek modelin gelecekte nasıl görüneceğini tahmin etmenize olanak tanır

KAYNAKÇA
•	https://en.wikipedia.org/wiki/Simple_linear_regression
•	https://dergipark.org.tr/en/download/article-file/187511
•	https://aws.amazon.com/tr/what-is/logistic-regression/
•	https://www.ibm.com/tr-tr/analytics/learn/linear-regression
•	https://www.scribbr.com/statistics/simple-linear-regression/#:~:text=What%20is%20simple%20linear%20regressio%20n,Both%20variables%20should%20be%20quantitative.
•	https://www.youtube.com/watch?v=4qVRBYAdLAo
•	https://www.cancankiran.com/makine-ogrenimi/
•	https://www.statology.org/linear-regression-real-life-examples/
•	https://maniksonituts.medium.com/how-to-build-a-machine-learning-model-715d7ecb3d02

