public class proje2 {

    static int[][] matris; // Global değişken
    // Değişkeni buraya yazdığımızda tüm fonksiyonlar buna erişebilir oldu.
    // Bir fonksiyondan değişşiklik yaptığımızda global olarak değişti..
    // başka bir fonksiyon tekrar bunu kullanacağı zaman son halini kullandı.

    public static void matrisDondurmeSaatYonu(int satirSayisi, int sutunSayisi, int[][] matris) {//saat yönünde döndürmek için bu metodu oluşturdum.
        int satirIlk = 0;// satırın başlangıç değerine 0 atadım.
        int sutunIlk = 0;//sütunun başlangıç değerine 0 atadım.
        int onceki;//satır ve sütun değerlerini değiştimeden önceki matrisi bu değişkenle temsil ettim.
        int suan;//satır ve sütun değerleri değiştirilen matrisi bu değişkenle temsil ettim.

        onceki = matris[satirIlk + 1][sutunIlk];//önceki matrisimi ilk satırın 1 fazlası ve sütünun ilk hali olarak tanımladım.

        for (int i = sutunIlk; i < sutunSayisi; i++) {//ilk satırı ilerletmek için for döngüsü oluşturdum. Sütünun başlangıç değerini sütun sayısına kadar ilerlettim.
            suan = matris[satirIlk][i]; // suanki matrisi oluşturdum, satırın başlangıç değeri satırIlki sütunlar i yi temsil etti. Bu durumda satırIlk hep sabit kalacak ve i sütün sayısına kadar artacaktı.
            matris[satirIlk][i] = onceki;//sayıyı her seferinde bir adım sağa kaydırabilmek için eski değerini tuttum.
            onceki = suan;//ve eski değeri şimdiki değere atadım.
        }
        satirIlk++;//satır sayısının artmasını sağladım. 
        for (int i = satirIlk; i < satirSayisi; i++) {//son sütunu ilerletmesi için for döngüsü oluşturdum.
            suan = matris[i][sutunSayisi - 1];//son sütun ilerlerken i satırın başlangıcı kabul edilir ve parametre olarak verilen satır sayısına kadar döngü ilerler.
            matris[i][sutunSayisi - 1] = onceki; //sayının son sütununu ilerletebilmek için eski değerini tuttum.
            onceki = suan;//ve eski değeri şimdiki değere atadım.
        }
        sutunSayisi--; //sütun sayısını 1 azalttım.
        if (satirIlk < satirSayisi) {
            for (int i = sutunSayisi - 1; i >= sutunIlk; i--) {//son satırı tersine ilerletiyor.
                suan = matris[satirSayisi - 1][i];//bu kodda matrisin en son satırında sağdan sola doğru bir adımlık yer değiştirme sağladım.
                matris[satirSayisi - 1][i] = onceki;//en son satırı 43, 90, 90, 80, 36 olan bir matris düşünelim, burada [4][3]=80 iken 36 nın bir adım sola kaymasıyla [4][3]=36 oluyor.
                onceki = suan;//böylece yeni önceki değerim şimdiki değerim olan 80 e eşit oluyor. Bu şekilde matris sola doğru her sütun indisi için ilerliyor.
            }
        }
        satirSayisi--;//satırı 1 azaltıyoruz.
        if (sutunIlk < sutunSayisi) {
            for (int i = satirSayisi - 1; i >= satirIlk; i--) {//ilk sütunu tersine ilerletiyor
                suan = matris[i][sutunIlk];//matrisin ilk sutununda aşağıdan yukarıya doğru 1 adımlık yer değiştirme sağladım.
                matris[i][sutunIlk] = onceki;//ilk sütunu 44 46 1 43 43 olan bir matris düşünelim, [3][0]=43 iken 43'ün bir adım yukarı çıkmasıyla  [3][0] yerine hemen altındaki diğer 43 değeri geliyor.
                onceki = suan;//böylece yeni önceki değerim şimdiki değerim olan 43 e eşit oluyor. Bu şekilde aşağıdan yukarı yer değiştirme sağlanıyor.
            }
        }
    }

    public static void matrisDondurmeSaatYonununTersi(int satirSayisi, int sutunSayisi, int[][] matris) {//kullanıcı saat yönünü 1 seçtiğinde bu kod çalışıyor. Burada yazdığım kodlarda saat yönüyle aynı mantıkta ilerliyor 
        int satirIlk = 0;
        int sutunIlk = 0;
        int onceki;
        int suan;

        onceki = matris[satirIlk + 1][satirSayisi - 1];

        for (int i = sutunSayisi - 1; i >= sutunIlk; i--) {//i yi azaltarak her seferinde sütun sayısını 1 azaltıyoruz, satırın başlangıç değeri olan satirIlk'i sabit tutarak 0 yapıyoruz
            //ve bu şekilde ilk satırı tersine ilerletiyoruz.
            suan = matris[satirIlk][i];
            matris[satirIlk][i] = onceki;//sayıyı her seferinde bir adım sola kaydırabilmek için eski değerini tuttum.
            onceki = suan;//ve eski değeri şimdiki değere atadım. 
        }
        satirIlk++;
        for (int i = satirIlk; i < satirSayisi; i++) {//ilk sütunu ilerleten kodlar...
            suan = matris[i][sutunIlk];
            matris[i][sutunIlk] = onceki;//ilk sütunu 83,95,61,88,84 olan bir matris düşünelim.[1][0]=95 iken aşağı doğru bir adımlık yer değiştirme gerçekleştiğinde [1][0] =83 olacaktır.
            onceki = suan;// ve eski değerimi şimdiki değere atadım. artık 83 95 in yerine geçti ve yeni önceki değerim 95 oldu ve bir sonraki döngüde önceki değer olarak 95 kullanıldı.
        }
        sutunIlk++;
        for (int i = sutunIlk; i < sutunSayisi; i++) {//son satırı ilerleten kodlar...
            suan = matris[satirSayisi - 1][i];
            matris[satirSayisi - 1][i] = onceki;// son satırı 84,52,2,36,74 olan bir matris düşünelim. [4][1]=52 iken sağa doğru bir adımlık yer değiştirme ile [4][1]=84 olucaktır.
            onceki = suan; //önceki değerimi şuanki değerime atadım ve böylelikle bir sonraki döngüde kullanılacak olan önceki değerim 52 oldu.
        }
        satirSayisi--;
        for (int i = satirSayisi - 2; i >= 0; i--) {//son sutunu tersine ilerleten kodlar...
            suan = matris[i][sutunSayisi - 1];
            matris[i][sutunSayisi - 1] = onceki;// son sütunu 97,23,97,74,36 olan bir matris düşünelim. [2][4]=97 iken yukarı doğru bir adımlık yer değiştirme ile [2][4]=74 oldu.
            onceki = suan;// önceki değerimi şuanki değerime atadım ve böylelikle bir sonraki döngüde kullanılacak olan "önceki" değerim 97 oldu.
        }
    }

    public static void matrisOlustur(int satirSayisi, int sutunSayisi, int aralik) {//Bu metodda matrisi oluşturdum.

        matris = new int[satirSayisi][sutunSayisi];// Ramde yer ayırdım.
        for (int i = 0; i < satirSayisi; i++) {//iç içe döngü kulllanarak birinci döngüyü satır sayısına kadar,
            for (int j = 0; j < sutunSayisi; j++) {//ikinci döngüyü sutun sayısına kadar ilerlettim.
                System.out.print((matris[i][j] = (int) (Math.random() * aralik)) + " ");//Print yapısı kullanarak matrisin içini random değerlerle doldurdum.
                //Aralık değişkeni oluşturdum bu değişkenle matrisin içindeki değerlerin hangi aralıkta olmasını istiyorsak değiştirebiliriz
            }
            System.out.println();//üstteki koşul sağlandığında bir satır boşluk bırakıldı. Döngü sonlanana kadar devam etti.
        }
        System.out.println("****************");

    }

    public static void matrisDondurme(int satir, int sutun, int yon, int aralik, int adimSayisi) {//Bunu uygulamayı çalıştıran metod olarak düşünerek yazdım. Ve case 1 de bu metodu çağırdım.

        if (matris == null) {//Matrisi null değişkenine eşitledim bu şekilde case 1 hata vermeden çalıştı.
            System.out.println("Lütfen önce matris oluşturun");//kullanıcıya hatası durumunda bu mesajı ilettim.
        } else {
            for (int i = 0; i < adimSayisi; i++) {//adım sayısını kullanıcı istediği gibi değiştirebileceği için for döngüsü kullanarak adım sayısına kadar ilerlettim.
                if (yon == 1) {// yön durumunu if yapısıyla kontrol ettim. 1 e eşitse saat yönünün tersine, -1 e eşitse saat yönünde dönecekti.
                    matrisDondurmeSaatYonununTersi(satir, sutun, matris);//burada 1 e eşit olduğu için saat yönünün tersi metodunu çağırdım.
                } else {
                    matrisDondurmeSaatYonu(satir, sutun, matris);//buradada else durumu oldu -1 eşitliğini düşünerek saat yönü metodunu çağırdım.
                }
            }

            // Matris yazdırma kodumu aynen buradada kullandım...
            for (int i = 0; i < satir; i++) {
                for (int j = 0; j < sutun; j++) {
                    System.out.print(matris[i][j] + " ");
                }
                System.out.println();
            }
        }
    }

    public static void main(String[] args) {//test sınıfım
        Scanner s = new Scanner(System.in);//kullanıcıdan almam gereken değerler için scanner objesi oluşturdum.
        int[] array = {5, 5, -1, 100, 2};//Bu kısımda arrayi proje kağıdında bize verilen gibi doldurdum.
        char islem = '0'; //karakter kontrolünü yapabilmek için işlemi char olarak tanımladım.
        do {//programın menüde çıkış yapana kadar sürekli çalışması için do - while döngüsü kullandım.
            System.out.println("*****");//Menü kısmımı oluşturdum.
            System.out.println("1.Uygulamayı çalıştır");
            System.out.println("2.Matris oluştur");
            System.out.println("3.Direction");
            System.out.println("4.Step number");
            System.out.println("5.Exit");

            islem = s.nextLine().charAt(0);//kullanıcının girdiği karakteri tanıması için charAt(0) verdim, bunu internetten araştırdım.
            if (islem >= '1' && islem <= '5') {//karakter kontrolüm için if yapısı kullandım.
                switch (islem) {//Menü tabanım için switch-case yapısını kullandım.
                    case '1': //Kullanıcı 1'e basarsa çalışacak olan case. Uygulamayı çalıştırmak için bu case'i oluşturdum.
                        matrisDondurme(array[0], array[1], array[2], array[3], array[4]);//Uygulamayı çalıştırmak için ana metodum olan matrisDondurme metoduma uygun arraylari parametre olarak vererek çağırdım.
                        break;
                    case '2'://Kullanıcı 2'ye basarsa çalışacak olan case. Matris oluşturmayı bu casede kullanıcıdan istedim.
                        matrisOlustur(array[0], array[1], array[3]);//Burada matrisOlustur metodunun içine uygun arraylari parametre olarak vererek çağırdım.
                        System.out.println("Matris oluşturuldu.");
                        break;
                    case '3'://Kullanıcı 3'e basarsa çalışacak olan case. Directionu bu casede kullanıcıdan istedim.
                        System.out.print("Yön(1: Saat Yönünün Tersi, -1: Saat Yönü):"); // olası yönleri kullanıcının seçimine sundum.
                        String yon = s.nextLine();//konsoldan -'li integer okuyamadığından dolayı yonü string olarak almayı tercih ettim.
                        if ("1".equals(yon)) {//içerik kıyaslaması yaptım.
                            array[2] = 1;// eğer yön 1'e eşitse array[2]'nin değeri 1 olacaktı.
                            System.out.print("Yön " + array[2] + " olarak ayarlandı");
                        } else if ("-1".equals(yon)) {
                            array[2] = -1;//Eğer yön -1'e eşitse array[2]'nin değeri -1 olacaktı. 
                            System.out.print("Yön " + array[2] + " olarak ayarlandı");
                        } else {
                            System.out.println("Hatalı giriş"); // İkiside değilse kullanıcı hata mesajı alacak.
                        }
                        break;
                    case '4'://kullanıcı 4 e basarsa, bu casede adım sayısını kullanıcıdan istedim.
                        System.out.print("Adım sayısı:");
                        array[4] = s.nextInt();//arrayi 4. elemanı olan adım sayısını kullanıcıdan aldım.
                        s.nextLine();// burda bir kez daha next line kullandım çünkü üstteki int sadece integerı okudu kullanıcı entera bastığında onu okumadı. NextLine ile onu okumasını sağladım.
                        System.out.print("Adım sayısı " + array[4] + " olarak ayarlandı");
                        break;
                    case '5':// Burada da kullanıcı çıkış yapmak istediğinde 5'e basarak çıkış yapabilmesini sağladım.
                        islem = '5';
                        System.out.println("Çıkış yapılıyor...");
                        break;
                }
            } else {// buradaki else en başta tanımladığım karakter kontrolü yapan if yapısının else'i. kullanıcı kontrolünü yaptığım karakterler dışında birşey girdiğinde hata mesajı aldı.
                System.out.println("Hatalı işlem");
            }

        } while (islem != '5');//Buradaki while ile işlemimin kullanıcı hata yapsa dahi exiti seçene kadar devam etmesini sağladım.

    }
}
