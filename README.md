# dotnet_interview
.net interview questions and answers

## Class ve Object Nedir ?
Sınıflar :
  - Verileri ve methodları içine alan kod bloğudur. Sınıflar sayesinde kod yapısı parçalara bölünür ve karmaşıklık azalır.
  - Bir sınıf kendisinde oluşturulacak nesneler için takım üyeler içermelidir.
  - Bu üyeler; alanlar (fields), metodlar (methods), yapıcılar (constructor), özellikler (properties), olaylar (events), delegeler (delegates) olarak sıralanabilir.
  - Örnek: Bir "Araba" sınıfı, arabanın özelliklerini (marka, model, hız) ve davranışlarını (hızlanma, fren yapma) tanımlayabilir.

Nesneler :
  - Sınıflardan üretilirler ve sınıfların aksine kimlikleri vardır.
  - Bir nesne kendi hakkında, yapabileceği işlemler ile ilgili bilgiler saklar. Programın gereksinim duyduğu tüm veriler nesneler tarafıdan tutulur.
  - Örnek: "Araba" sınıfından türetilen bir "Toyota Corolla" nesnesi, belirli bir arabanın özelliklerini ve davranışlarını temsil eder.

## Managed ve Unmanaged Code
Managed Code :
  - CLR (Common Language Runtime) tarafından yürütülen bir koddur. Compiler tarafından derlenmiş koddur.
  - .NET framework tarafından yönetilen ve makine koduna dönüştürülmeden önce ara bir dile çeviren kod bloğududur.
  - Çalışma zamanı (runtime) tarafından otomatik olarak bellek yönetimi, hata denetimi ve güvenlik kontrolleri gibi işlemlerle desteklenir. Bu nedenle, programın daha güvenli ve istikrarlı olmasına yardımcı olur.

Unmanaged Code : 
  - .NET dışındaki herhangi bir framework ile çalışma zamanı tarafından kontrol edilmeyen ve yönetilmeyen kod türünü ifade eder.
  - Genellikle derlenmiş dil (compiled language) veya C/C++ gibi dillerle ilişkilendirilir. Bu tür diller, doğrudan bellek yönetimi ve işletim sistemi kaynaklarına erişim sağlar.

## C# Kod Derleme Aşamaları
İlk adım, C# programınızın kaynak kodunu yazmaktır. Kaynak kod, C# programınızın mantığını ve davranışını tanımlar. Bu kod Visual Studio, Visual Studio Code veya başka bir C# geliştirme ortamında yazılabilir.

Proprocessing :
  - Kaynak kod, önişlem aşamasından geçer. Bu aşamada #include veya #define gibi önişlem direktifleri işlenir.

Compilation :
  - C# kaynak kodunun derlenmesidir. C# derleyicisi bu adımda devreye girer.
  - Derleyici, kaynak kodunuzu alır ve onu çalışabilir bir formata çevirir. Bu aşamada syntax hataları ve mantıksal hatalar tespit edilir.
  - Sonuç olarak, derlenmiş bir program veya kütüphane (genellikle bir .exe veya .dll dosyası) oluşturulur (out generation). Bu derlenmiş kod "Managed Code" olarak adlandırılır.

Linking :
  - Eğer projeniz birden fazla dosya veya modül içeriyorsa, bu aşamada bu dosyalar bir araya getirilir ve bağlanır.
  - Bu, projenin farklı bileşenlerinin birleştirilip bir bütün haline getirilmesini sağlar.
  - Linking işlemi, derlenmiş kodun daha büyük projelerde düzgün çalışabilmesi için önemlidir.

Common Language Runtime :
  - CLR (Common Language Runtime), .NET Framework veya .NET Core gibi platformlarda C# programlarının çalıştırılmasını sağlayan temel bileşendir.
  - CLR, derlenmiş kodu çalıştıran ve yöneten bir çevre sunar. Bu çevre, kodun çalıştırılması, bellek yönetimi, hata yönetimi ve güvenlik kontrolleri gibi işlevleri sağlar.

Execution :
  - CLR tarafından yüklenen derlenmiş kod (Managed Code), runtime sırasında yürütülür.
  - Yani, kullanıcı veya otomatik bir süreç tarafından başlatılan program, CLR içinde çalıştırılır.
  - CLR, programın veri işleme ve kontrol akışını yönetir.

## Temel OOP Kavramları
Kapsülleme :
  - Bir nesnenin bazı özellik ve işlevleri, başka sınıf ve nesnelerden gizlenir.
  - Veri uygulamasının geri kalanı gizlenirken yalnızca gerekli bilgilere erişilebilir.
  - Bu, verilerin doğrudan erişimini engeller ve sınıfın iç mantığına erişimi kontrol eder.

Soyutlama :
  - Bir nesnenin kritik davranışını ve verilerini belirleme ve ilgisiz detayları ortadan kaldırma işlemidir.

Kalıtım :
  - Bir sınıfın başka bir sınıftan özelliklerini ve davranışlarını devralmasını sağlayan bir mekanizmadır.
  - Bu, kodun yeniden kullanılabilirliğini artırır ve sınıflar arasında bir hiyerarşi oluşturabilir.

Polimorfizm :
  - Aynı adı taşıyan metotların farklı sınıflarda farklı şekillerde davranabilmesini ifade eder.
  - Bu, bir arayüzün veya temel sınıfın alt sınıflarında farklı şekillerde uygulanabilmesini sağlar.

## "using" İfade Nedir ?
  - Belirli bir namespace'i içe aktararak (import ederek) o namespace içindeki sınıf ve öğelere daha kolay erişim sağlar.
  - Örneğin, System namespace'ini içe aktararak, Console.WriteLine() gibi System namespace'i içinde tanımlanan sınıf ve metotlara daha kısa bir şekilde erişebilirsiniz.
  - C# projelerinde harici sınıf kütüphanelerini veya assembly'leri kullanmak için using ifadesi kullanılabilir.
  - Bu şekilde, başka bir projede veya pakette bulunan sınıflara erişim sağlanabilir. Özellikle, NuGet paketleri gibi harici kütüphaneler projeye eklenirken using ifadesi kullanılır.

## Regular Expression
  - Regular expression, sayısal ve string ifadenin belirli kurallara uyumluluğunu kontrol etmeye ve düzenlemeye yarar.
  - Regex, dize ayrıştırmanın yanı sıra karakter dizesini değiştirmek için de kullanılır.
  - Metin tabanlı verileri belirli bir desene göre aramak, eşleştirmek ve manipüle etmek için kullanılan güçlü bir metin işleme aracıdır.
  - Regex ifadeleri, metin analizi, metin ayıklama, veri doğrulama, düzenleme ve dönüştürme gibi birçok farklı uygulama alanında kullanılabilir.

## Class vs Struct 
Class :
  - Inheritance destekler.
  - Reference type
  - Üyeleri default olarak private
  - Büyük ve karmaşık modeller için

Struct :
  - Inheritance desteklemez.
  - Value type
  - Üyeleri default olarak public
  - Küçük ve izole modeller için

## Exception Handling
Try - Catch : 
  - Hata Yönetimi, try ve catch blokları aracılığıyla gerçekleştirilir. Kod, try bloğunda çalıştırılır ve eğer bir hata meydana gelirse, bu hata catch bloğunda ele alınır. 

Finally :
  - Bir istisnanın yakalanıp yakalanmadığına bakılmaksızın çalıştırılmak üzere yazılmış bir kod bloğudur.

Throw :
  - Bir sorun oluştuğunda bir istisna atar.

## Constructor ve Destructor Kavramları
Constructor(Yapıcı Metot) :
  - Bir sınıfın bir nesnesi (instance) oluşturulduğunda otomatik olarak çalışan özel bir metottur.
  - Constructor, sınıf adı ile aynı isimde olmalıdır.
  - Parametre alabilir veya parametresiz olabilir. Overload edilebilir. Geriye değer döndürmezler. 

  ```
      class Person
    {
        public string Name;
        public int Age;
    
        // Parametresiz constructor
        public Person()
        {
            Name = "Unknown";
            Age = 0;
        }
    
        // Parametre alan constructor
        public Person(string name, int age)
        {
            Name = name;
            Age = age;
        }

        // Destructor tanımı
        ~PersonDestructor()
        {
            // Nesne yıkıldığında buraya gelinir
            // Kaynakları serbest bırakmak için kullanılabilir
        }
    }
    
    // Nesne oluşturma ve constructor kullanımı
    Person person1 = new Person(); // Parametresiz constructor
    Person person2 = new Person("Alice", 30); // Parametre alan constructor

  ```

Destructor(Yıkıcı Metot) :
  - Bir nesne ömrü sona erdiğinde (garbage collector tarafından toplandığında) otomatik olarak çalışan metottur.
  - C# programlama dilinde, ~ (tilde) işareti ile başlayan bir metot adı ile tanımlanır.
  - Genellikle unmanaged kaynakları (bellek, dosya işlemleri, bağlantılar vb.) serbest bırakmak için kullanılır.
  - C# programcıları genellikle Destructorları özel olarak tanımlamak zorunda kalmazlar, çünkü çoğu zaman .NET çöp toplayıcı (garbage collector) bu kaynakları yönetir.

## Boxing ve Unboxing nedir?
Değer tiplerinin referans tipine dönüşmesine kutulama (boxing), referans tiplerin değer tipine dönüşmesine ise kutu-açma (unboxing) denir.

## Jagged Array
Jagged Arrays, elemanları dizi olan bir dizidir. Boyutları tek veya birden fazla olabilir.

  ```
    int[ ][ ] jaggedArr = new int[3][ ];
  ```

## Access Modifiers
Private :
  - Tanımlanan değişkene sadece kendi class’ı içinden ulaşılabileceği anlamına gelmektedir. Kesinlikle değiştirilmemesi gereken kodlarda kullanılmaktadır.
    
Public :
  -  Kod içinde herhangi bir yerden erişilebilir durumda olmasını sağlar. Public erişim belirleyici tipinde kısıtlama yoktur.
    
Protected :
  - Bulunduğu class ve o class üzerinden türetilen sınıflar içinden erişilebilir olduğunu göstermektedir.

Internal :
  - Aynı program(proje) içerisinden erişilebilir fakat farklı program içerisinden erişilemez. Program içerisinde herhangi bir kısıtlaması yoktur.

Protected Internal :
  - Bir üyenin hem kendi sınıfı içinde hem de aynı derleme (assembly) içindeki diğer sınıflardan erişilmesine izin verir.

NOT: "internal" sınıf üyelerine sadece aynı derleme içindeki diğer sınıflar erişebilirken, "protected internal" ise aynı derleme içindeki diğer sınıfların yanı sıra türetilmiş sınıfların da erişmesine izin verir.

## Dispose Metodu
  - Yönetilmeyen kaynakların serbest bırakılması için kullanılır. Dispose yöntemi programcının kaynakların verimli kullanımı için manuel olarak uygulaması gerekir.
  - .NET Framework'teki IDisposable arabirimini uygulayan sınıflarda genellikle kullanılan bir metottur. Bu metod, sınıfın kaynaklarını serbest bırakmak ve gerektiğinde belleği temizlemek için kullanılır.
  - Özellikle unmanaged kaynakları (örneğin dosya işlemleri, ağ bağlantıları veya veritabanı bağlantıları gibi) düzgün bir şekilde serbest bırakmak için kullanılır.

## Static ve Void
Static :
  - Bir sınıf üyesi (alan, metot, özellik) static olarak işaretlendiğinde, bu üye sınıfın bir örneği (instance) oluşturulmadan doğrudan sınıf adıyla erişilebilir.
  - static üyeler, tüm örnekler (instance) arasında paylaşılır ve bu nedenle tüm örnekler için aynı değeri veya davranışı temsil eder.
  - Genellikle yardımcı metotlar, sabit değerler veya örneklerle bağlantılı olmayan işlevselliği ifade etmek için kullanılır.

Void :
  - void dönüş tipine sahip bir metot bir değer üretmez, sadece belirli bir işlemi gerçekleştirir.
  - void dönüş tipi, genellikle bir metotun sonuç döndürmesi gerekmediğinde veya sadece yan etki (side effect) üreteceğinde kullanılır.

## Delegate ve Multi Delegate
Delegate :
  - Bir metot imzasını temsil eden ve bu metotları işaret edebilen bir türdür.
  - Bir metot referansıdır ve bu referans, belirli bir metodu çağırmak için kullanılabilir.
  - Bir olayın abone edilmesi (subscribe) veya callback işlevleri gibi senaryolarda kullanılır.

    ```
    // Delege tanımı
    public delegate void MyDelegate(string message);
    
    // Delege'ye bir metot atama
    MyDelegate delegateInstance = Console.WriteLine;
    
    // Delege ile metot çağırma
    delegateInstance("Merhaba, Dünya!");
    ```

Multicast Delegate :
  -  Birden fazla metodu aynı anda çağırmak için kullanılan bir Delegate türüdür.
  -  Birden fazla metot referansını içerebilir ve bu referanslardan her biri çağrıldığında ilgili metotlar sırayla çalıştırılır.
  -  += operatörü ile birden fazla metot referansı Multicast Delegate'e eklenir ve -= operatörü ile çıkarılır.

    ```
    public delegate void MyDelegate(string message);

    class Program
    {
        static void Main()
        {
            MyDelegate multicastDelegate = Method1;
            multicastDelegate += Method2;
            multicastDelegate += Method3;
    
            multicastDelegate("Merhaba, Dünya!");
    
            // Çıktı:
            // Method1: Merhaba, Dünya!
            // Method2: Merhaba, Dünya!
            // Method3: Merhaba, Dünya!
        }
    
        static void Method1(string message)
        {
            Console.WriteLine("Method1: " + message);
        }
    
        static void Method2(string message)
        {
            Console.WriteLine("Method2: " + message);
        }
    
        static void Method3(string message)
        {
            Console.WriteLine("Method3: " + message);
        }
    }
    ```

## Value Type ve Reference Type
Value Type :
  - "Value type" veriler, değerlerini doğrudan içerir ve bellekte "stack" adı verilen veri yapısında saklanır.
  - Değer türü değişkenleri, bellekteki değerleri kopyalayarak çalışır. Yani bir değer türü değişkeni başka bir değişkene atandığında, değerler kopyalanır ve bağımsızdır.
  - int, float, char, bool, struct gibi veri türleri değer türlerine örnektir.
  - Değer türü değişkenler, hızlıdır ve değerlerin kopyalanmasına dayalıdır.

Reference Type :
  - "Reference type" veriler, değerlerinin bellekteki bir referansa (adrese) işaret ettiği bir "heap" adı verilen veri yapısında saklanır.
  - Referans türü değişkenleri, değerleri yerine bu değerlerin bellekteki adreslerini (referanslarını) saklarlar.
  - Bu nedenle bir referans türü değişkeni başka bir değişkene atandığında, aynı bellek alanını işaret ederler.
  - string, sınıflar (class), diziler (array), object gibi veri türleri referans türlerine örnektir.
  - Referans türü değişkenler, bellekte dinamik olarak yönetildiği için daha fazla esneklik sunar ancak değer türleri kadar hızlı değildir.

NOT : string veri tipi reference type olarak geçse de davranış olarak value type gibi davranır.

NOT : Koleksiyon sınıfları reference tipindedir; veri depolama ve erişim için kullanılan sınıflardır. Bu sınıflar System.Collections.Generic ad alanında(namespace) bulunur.

## Coalescing Operator
Tek satırda null check ve varsayılan değer atama işlemini yapabileceğimiz bir operatördür. (name = name ?? "default";)

## Abstract Class vs Interface 
Abstract :
  - Hem somut (concrete) metotlar hem de soyut (abstract) metotlar içerebilen bir sınıf türüdür.
  - Somut metotlar, özelleştirilmiş uygulamaları içerir ve alt sınıflar tarafından doğrudan kullanılabilir.
  - Soyut metotlar ise sadece metot başlıklarını (imzalarını) içerir ve alt sınıflar bu metotları zorunlu olarak uygulamak zorundadır.
  - Bir sınıf yalnızca bir soyut sınıfı miras alabilir.

Interface :
  - Sadece metot başlıklarını (imzalarını) içeren ve herhangi bir özelleştirilmiş olayı içermeyen bir yapıdır.
  - Arabirimler, birden fazla sınıf tarafından aynı anda implement edilebilir (bir sınıf birden fazla arabirimi implement edebilir).

## Sealed ,Virtual, Static ve Override Kavramları
Sealed :
  - Miras(Inheritance) alınmasını istemediğiniz sınıflar için kullanabileceğiniz bu keyword sayesinde kullanılan class hiçbir şekilde başka bir class’a miras olarak geçilemez.
  - Özetle Sealed; sınıflar için kalıtım yapmayı, üyeler için ise override edilmeyi önler.

Virtual :
  - Sınıf içerisinde sanallaştırmak istediğimiz yani çakışma durumunda veya gövdesinin gerçekleştirdiği işlemin uygun olmadığını  düşündüğünüz zaman ezmek istediğimiz metot türleridir.
  - Bir metot virtual olarak işaretlendiğinde, bu metotun alt sınıflar tarafından yeniden yazılması (override) ve değiştirilmesine izin verilir.

Static :
  - Static olarak tanımlanan üyeler(class, property, field) ram’de tek seferlik bir tanım yapılması sağlanır ve her okuma işleminde ram’deki bu kaynaktan doğrudan okunması sağlanır.
  - Class özelinde static tanımını şöyle yapabiliriz; Bir instance almaya gerek duymadan doğrudan static olarak tanımlanmış sınıfın üyelerine erişilebilir ve değer ataması yapılabilir.

Override :
  - override anahtar kelimesi bir alt sınıfta, üst sınıfın (baz sınıfın) sanal (virtual) bir metot veya özellik (property) üzerine yeni bir uygulama sağladığını belirtir.
  - Alt sınıftaki override metodu, temel sınıftaki virtual metodu ile aynı imzaya (metodun ismi, parametreleri ve dönüş tipi) sahip olmalıdır.

## Design Patterns
Tasarım deseni (Design Pattern), yazılım geliştirme süreçlerinde karşılaşılan sorunları çözmek için oluşturulmuş tekrar kullanılabilir çözüm şablonlarıdır. 
Yazılımın daha sürdürülebilir, esnek ve anlaşılabilir olmasına yardımcı olur.

1. Creational (Yaratıcı) Pattern
   - Bu desenler, nesnelerin nasıl oluşturulacağına ve başlatılacağına odaklanır. Örnekler arasında Singleton, Factory Method ve Builder bulunur.

2. Behavioral (Davranışsal) Pattern
   - Bu desenler, nesnelerin nasıl bir araya getirileceği ve oluşturulacağına odaklanır. Örnekler arasında Adapter, Decorator ve Bridge bulunur.

3. Structural (Yapısal) Pattern
   - Bu desenler, nesnelerin nasıl işbirliği yapacağına odaklanır. Örnekler arasında Observer, Strategy ve Command bulunur.
  










